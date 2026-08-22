# EXPERIMENT 04 - GAE LAUNCHER

## AIM

To use the **Google App Engine (GAE) Launcher** to launch web applications.

---

## SOFTWARE REQUIRED

* Google Cloud Console
* Google Cloud SDK
* Google App Engine
* Web Browser
* Text Editor
* Internet Connection

---

## PROCEDURE

### 1. Create or Select a Cloud Console Project

1. Create a new Cloud Console project or select an existing project.
2. Note the **Project ID** of the project.
3. Open the project page in Google Cloud Console.

### 2. Install Google Cloud SDK

1. Download the Google Cloud SDK.
2. Install the SDK on the system.
3. Initialize the Google Cloud SDK.
4. Select or configure the required Cloud project.

### 3. Create the Web Application

Create the basic project structure:

```
Project/
|
+-- app.yaml
|
+-- www/
    |
    +-- index.html
    |
    +-- css/
    |   |
    |   +-- style.css
    |
    +-- images/
    |
    +-- js/
```

The `app.yaml` file is used to configure the App Engine application and
map URLs to the required static files.

---

### 4. Create app.yaml

Create an `app.yaml` file in the root directory of the application.

Example configuration from the lab manual:

```
runtime: python27
api_version: 1
threadsafe: true

handlers:
- url: /
  static_files: www/index.html
  upload: www/index.html

- url: /(.*)
  static_files: www/\1
  upload: www/(.*)
```

---

### 5. Create index.html

Create `index.html` inside the `www` directory.

Example:

```
<html>
<head>
    <title>Hello, world!</title>
    <link rel="stylesheet" type="text/css"
          href="/css/style.css">
</head>

<body>
    <h1>Hello, world!</h1>

    <p>
    This is a simple static HTML file that will be served
    from Google App Engine.
    </p>
</body>
</html>
```

---

### 6. Deploy the Application

Open a terminal in the project root directory where `app.yaml`
is located.

Run:

```
gcloud app deploy
```

Optional project specification:

```
gcloud app deploy --project YOUR_PROJECT_ID
```

Optional version specification:

```
gcloud app deploy -v YOUR_VERSION_ID
```

---

### 7. Launch the Web Application

After successful deployment, launch the application using:

```
gcloud app browse
```

The application can be accessed using the App Engine URL:

```
https://PROJECT_ID.REGION_ID.r.appspot.com
```

---

## PROJECT STRUCTURE

```
Project/
|
+-- app.yaml
|
+-- www/
    |
    +-- index.html
    |
    +-- css/
    |   |
    |   +-- style.css
    |
    +-- images/
    |
    +-- js/
```

---

## WORKFLOW

```
Create Cloud Project
        |
        v
Install Google Cloud SDK
        |
        v
Create Web Application
        |
        v
Create app.yaml
        |
        v
Create index.html
        |
        v
Deploy using gcloud app deploy
        |
        v
Launch using gcloud app browse
        |
        v
Web Application Successfully Launched
```

---

## EXPECTED OUTPUT

The web application should display:

```
Hello, world!
```

The application should be accessible through the deployed
Google App Engine URL.

---

## RESULT

Thus, the **GAE Launcher was used successfully to launch the
web application**.

---

## EXPERIMENT DETAILS

Experiment No. : 04
Experiment Name : Use GAE Launcher to Launch Web Applications
Platform        : Google App Engine
SDK             : Google Cloud SDK
Configuration   : app.yaml
Application     : Static Hello World Web Application
Status          : Completed

---
