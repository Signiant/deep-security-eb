# deep-security-eb
Elastic Beanstalk extension to install and configure Trend Micro Deep Security as a service

This beanstalk extension is a bit more robust than the example from Trend in that it handles timeouts when trying to register with the DSM.  It also allows custom specification of a policy as well as not hard-coding the tenantID and password.

On a new deployment of code containing the extension, it will download and install the agent.  On subnsequent deployments, it will trigger a recommendation scan (with the logic being that the environment could have changed).


## Usage
Include the extention file as per EB documentation on extensions

## Variables

Your beanstalk will need 3 variables:

*   DS_TENANTID - your tenantID from Deep Security as a service
*   DS_TENANTPW - your tenant password from Deep Security as a service
*   DS_POLICY - the name of the policy to assign to all instances in this beanstalk environment

