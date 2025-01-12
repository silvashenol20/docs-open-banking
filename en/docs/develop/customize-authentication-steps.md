This section explains how to customize the default authentication steps according to your requirements. 

The Adaptive Authentication script for the solution is available at `<IS_HOME>/repository/conf/common.auth.script.js`. 
You can customize this script and implement the required modules accordingly.

## Customize the Application Management Listener

The default Application Management Listener in WSO2 Open Banking Accelerator supports configuring only one primary local 
authenticator and only one federated authenticator for regulatory service providers. Therefore, customize it by 
overriding the default [Application Management Listener](application-management-listener.md)
according to your requirements:

1. Customize the following methods:

    - `setAuthenticators` method: override this method to configure any number of authentication steps and read the relevant 
       authenticator configurations via the toolkit configuration file.
    - `setConditionalAuthScript` method: override this method to read your custom `common.auth.script.js` from a configured 
       location.

2. Build and configure the customized JAR file according to the 
[Application Management Listener](application-management-listener.md#configuring-a-custom-application-management-listener)
documentation.

3. Add your customized `common.auth.script.js` file to the configured location.

4. Add the authenticator configurations based on your requirements.

For more information, see the [Application Management Listener](application-management-listener.md) documentation. 


