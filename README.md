# TDD Java Intro

Quick intro to get started with TDD and simple design using Java.

You probably want to disable Copilot or any other AI plugin to be able to practice TDD. Otherwise, once the test name is written, the AI will suggest its implementation.

## Setup

> 💡 It is highly encouraged and recommended to install and use [IntellIJ Community Edition](https://www.jetbrains.com.cn/en-us/idea/download/other.html) as IDE (pick the last version available).

Java 21 is required to run this project. Below are the steps to install it locally or using [SDKMan!](https://sdkman.io/) (recommended).

### Local Installation

1. Go to the [Adoptium website](https://adoptium.net/es/temurin/releases/) and select **JDK 21** for **Windows x64 (.msi)**.
2. Double-click the downloaded `.msi`, accept the license terms, and keep the default install path (e.g. `C:\Program Files\Eclipse Adoptium\jdk-21`).
3. Set the `JAVA_HOME` environment variable
   - Open **Control Panel → System → Advanced system settings → Environment Variables**.
   - Under **System variables**, click **New** (or **Edit** if it already exists) and set:
     
     - **Variable name:** `JAVA_HOME`
     - **Variable value:** your install path, e.g. `C:\Program Files\Eclipse Adoptium\jdk-21`
4. Verify the installation opening a command prompt and running `java -version`. You should see output indicating version 21.x

### Using SDKMan! 

1. Open PowerShell as **Administrator** and run `wsl --install`. Then reboot. By default, this installs Ubuntu under WSL2.
2. From the Start menu, type **Ubuntu** and complete the initial user setup.
3. In the Ubuntu shell, run:
    ```
    curl -s "https://get.sdkman.io" | bash
    source "$HOME/.sdkman/bin/sdkman-init.sh"
    ```
4. Install Temurin 21 via SDKMan!
    ```
    sdk install java 21.0.7-tem
    ```
   When prompted, agree to make it your default Java.
5. In Ubuntu, run `java -version` to confirm you're using Java 21.

## Run tests

You can run the tests by running:

`./gradlew test`
