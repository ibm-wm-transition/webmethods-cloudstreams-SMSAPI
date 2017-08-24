# webMethods CloudStreams Provider for SMSAPI.com
This project provides a sample webMethods CloudStreams Provider Project for SMSAPI.com. The following APIs are available:
* **Send SMS:** SMSAPI is a high quality SMS platform which enables you to integrate any of your applications with our
SMS message sending and receiving system. https://www.smsapi.com/assets/files/SMSAPI_http_en.pdf
* **Check Balance:**: Current account balance may be checked using one of the extended function. https://www.smsapi.com/assets/files/SMSAPI_http_en.pdf

## Requirements

The project was developed and tested on the following installation:
1. Integration Server 9.12
2. CloudStreams Server 9.12
3. Software AG Designer 9.12 with Service Development and CloudStreams Development

## Quick start

To install the project on your local development environment follow these steps.

### Prepare CloudStreams connection

1. In Software AG Designer open ```Window > Preferences```.
2. Navigate to ```Software AG > CloudStreams Servers```.
3. Add your local Integration Server. If there is already an entry make sure username and password are correct by clicking the Test button.

### Import CloudStreams Provider Project

1. In Software AG Designer switch to the ```CloudStreams Development``` perspective.
2. Select File > Import and choose ```Software AG > CloudStreams Provider Project```. Click Next.
3. Select the root of this repository as the Root Directory.
4. Select the ```SMSAPI``` project.
5. Check ```Copy project into workspace```.
6. Click Finish.
7. Expand the newly imported project.
8. Right-click ```com.softwareag.smsapi``` and select Deploy.

### Import Integration Server packages
The CloudStreams Provider Project does not contain neccessary doctypes.

1. Copy SMSAPI.zip and SMSAPITests.zip to ```<install_dir>/IntegrationServer/instances/<instance>/replicate/inbound```.
2. Open Integration Server Administration in your browser.
3. Install both packages with ```Install Inbound Releases``` in Package Management.

### Add SMSAPI.com Username and Password and activate connection

To access SMSAPI.com a username and password is neccessary. Generate your SMSAPI.com Trial account here: https://www.smsapi.com/.

1. Open Integration Server Administration in your browser.
2. Navigate to ```Solutions > CloudStreams > Providers > SMSAPI```.
3. Select ```com.softwareag.smsapi``` from the Connector List.

You will find one (disabled) connection: wmsmsapiTests:connection. You need to modify this connections:
1. Click the Edit button of the connection.
2. Enter your username and password and save the changes.
3. Enable the connection.

### Run tests

1. In Software AG Designer switch to the ```Service Development``` perspective.
2. Expand the ```SMSAPITests``` package.
3. Run the ```*Test``` flow services you find in the subsequent directories.
______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________
Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.
