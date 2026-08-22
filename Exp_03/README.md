# EXPERIMENT 03 - GOOGLE APP ENGINE

---

## AIM

To install **Google App Engine (GAE)** and create a **Hello World application** and other simple web applications using Python/Java.

---

## SOFTWARE REQUIRED

* Google App Engine
* Google Plugin for Eclipse
* Eclipse IDE
* Google App Engine Java SDK
* Java / Python
* Web Browser
* Google Account

---

## PROCEDURE

### 1. Install Google Plugin for Eclipse

1. Install the **Google Plugin for Eclipse**.
2. Install the **Google App Engine Java SDK** along with the plugin.
3. If the SDK is not installed with the plugin, download the Google App Engine Java SDK separately.
4. Extract the SDK files.

---

### 2. Create a New Web Application Project

1. Open **Eclipse IDE**.
2. Click the **Google** icon in the Eclipse toolbar.
3. Select **New Web Application Project**.
4. Configure the Google Web Application project.
5. Link the Google App Engine Java SDK using the **Configure SDK** option.
6. Click **Finish**.

The Google Plugin for Eclipse generates a sample project automatically.

---

### 3. Review the Project Structure

The generated project follows a standard Java web project structure.

```text
HelloWorld/
│
├── src/
│   └── Java source code
│
├── META-INF/
│   └── Configuration files
│
└── war/
    ├── JSPs
    ├── Images
    ├── Data files
    │
    └── WEB-INF/
        ├── Application configuration
        ├── lib/
        │   └── JAR libraries
        │
        └── classes/
            └── Compiled classes
```

The project also contains the `appengine-web.xml` configuration file required by Google App Engine.

---

### 4. Configure `appengine-web.xml`

The `appengine-web.xml` file is used to configure the application for Google App Engine.

Example:

```xml
<?xml version="1.0" encoding="utf-8"?>

<appengine-web-app xmlns="http://appengine.google.com/ns/1.0">
    <application></application>
    <version>1</version>

    <system-properties>
        <property
            name="java.util.logging.config.file"
            value="WEB-INF/logging.properties"/>
    </system-properties>
</appengine-web-app>
```

---

### 5. Run the Application Locally

1. Right-click the project in Eclipse.
2. Select **Run As → Web Application**.
3. The development server starts.
4. Open the application using:

```text
http://localhost:8888/
```

The manual also provides the Hello World servlet URL:

```text
http://localhost:8888/helloworld
```

---

### 6. Deploy to Google App Engine

1. Register/sign in with a Google account.
2. Create an application ID for the web application.
3. Add the application ID to `appengine-web.xml`.
4. Use the **GAE Deploy** option in Eclipse.
5. Sign in with the Google account when prompted.
6. Click **Deploy**.

The application is then deployed to Google App Engine.

---

## APPLICATION CONFIGURATION

Example:

```xml
<appengine-web-app xmlns="http://appengine.google.com/ns/1.0">
    <application>YOUR_APPLICATION_ID</application>
    <version>1</version>
</appengine-web-app>
```

Replace `YOUR_APPLICATION_ID` with the application ID created for the project.

---

## PROJECT STRUCTURE

```text
HelloWorld/
│
├── src/
│
├── META-INF/
│
└── war/
    ├── WEB-INF/
    │   ├── lib/
    │   └── classes/
    │
    ├── JSP files
    ├── Images
    └── Data files
```

---

## WORKFLOW

```text
Install Google Plugin
        │
        ▼
Install / Configure GAE SDK
        │
        ▼
Create Web Application
        │
        ▼
Create Hello World Application
        │
        ▼
Configure appengine-web.xml
        │
        ▼
Run Locally
        │
        ▼
Test using localhost
        │
        ▼
Create Application ID
        │
        ▼
Deploy to Google App Engine
        │
        ▼
Web Application Successfully Deployed
```

---

## EXPECTED OUTPUT

The Hello World web application should run successfully on the local development server.

```text
http://localhost:8888/
```

The Hello World servlet can also be accessed using:

```text
http://localhost:8888/helloworld
```

## After deployment, the application becomes accessible through its Google App Engine application URL.

## RESULT

Thus, **Google App Engine was installed successfully, a Hello World web application was created, tested locally, and deployed successfully in Google App Engine.**

---

## EXPERIMENT DETAILS

| Property            | Details                   |
| ------------------- | ------------------------- |
| **Experiment No.**  | 03                        |
| **Experiment Name** | Install Google App Engine |
| **Application**     | Hello World               |
| **IDE**             | Eclipse                   |
| **Platform**        | Google App Engine         |
| **SDK**             | Google App Engine SDK     |
| **Status**          | Completed                 |

---
