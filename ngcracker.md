ng-cracker is a simple library for cracking Angular application components. It is generally used for accessing or extracting information from Angular applications, typically in a debugging or penetration testing context. Below, I'll walk you through the process of installing and using ng-cracker with an example of how you can use it to inspect an Angular application.
## Prerequisites:

    Node.js installed.
    npm (Node Package Manager) installed.
    Basic knowledge of Angular and how Angular applications are structured.

### Step 1: Install ng-cracker

First, install ng-cracker from npm (Node Package Manager). Open your terminal and run the following command:
```bash
npm install -g ng-cracker
```
This command will install the ng-cracker globally so you can use it in any Angular application.
### Step 2: Set up an Angular Application

If you don’t have an Angular application set up already, you can create one using Angular CLI.
```bash
ng new angular-cracker-example
cd angular-cracker-example
```
After this, create a simple Angular app with a component to interact with ng-cracker.
```bash
ng serve
```
Now, your Angular application is running on http://localhost:4200.
### Step 3: Using ng-cracker

`ng-cracker` works by inspecting the DOM of an Angular application and extracting useful data from it. Here's an example of how to use ng-cracker.

In a new terminal window, run the following command:
```bash
ng-cracker http://localhost:4200
```
This will connect to your Angular app running locally and attempt to gather some useful information about the application.
Example Output:

You will see output similar to this:
```bash
[INFO] Scanning http://localhost:4200
[INFO] Angular version: 12.0.0
[INFO] Found Components:
  - AppComponent
  - HomeComponent
  - AboutComponent
[INFO] Found Services:
  - DataService
  - AuthService
[INFO] Found Modules:
  - AppModule
  - HomeModule
```

### Step 4: Inspect Specific Data

You can pass additional parameters to ng-cracker to extract specific types of information. For example, to list all components, you can use:
```bash
ng-cracker http://localhost:4200 --components
```
This will give you a detailed list of the components in your Angular application.
### Step 5: View Component Details

You can get more details about a specific component. For example:
```bash
ng-cracker http://localhost:4200 --component HomeComponent
```
This will output all relevant details about the HomeComponent, such as its metadata, selector, inputs, and other attributes.
### Step 6: Using ng-cracker in Production

Once your Angular app is deployed to a production server, you can also use ng-cracker to inspect the app. Make sure you have access to the hosted app, and then run:
```bash
ng-cracker https://your-angular-app.com
```
This will perform the same analysis but remotely, which can be helpful for penetration testing or security auditing of public Angular applications.
### Step 7: Security Considerations

    ng-cracker can potentially expose sensitive data about your Angular application, such as the components, services, and other application internals. It's recommended not to use it on production environments unless you're authorized to do so.

    Always ensure that your Angular app is properly secured and protected from unauthorized access.

### Conclusion

In this tutorial, you've learned how to use ng-cracker to inspect Angular applications. It's a helpful tool for developers and security auditors to examine the structure of an Angular application. However, it should be used responsibly and ethically to avoid misuse or security breaches.

For further details on usage or advanced options, you can refer to the official documentation of ng-cracker on its GitHub or npm page.


