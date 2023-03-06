# node-for-log4j
Provides the ACE / IIB / WMB message flow processing node for log4j formerly known as SupportPac IAM3.
It provides the ability to use the log4j logging framework from within your ACE / IIB / WMB flows.

## Description
This SupportPac allows a message flow to log information using the log4j logging framework. This way it is possible to set a log level for each log message and any destination target that can be defined using log4j.

The target as well as the runtime log level can be configured independent from the flow in the log4j configuration file.

## Possible Uses
Use this SupportPac if you need a more flexible logging mechanism than the Trace node provides.

## New in this Release
New in 2.0.2:
* reenable configurable properties

New in 2.0.1:
* prevent NullPointerException if logLevel is DEBUG

New in 2.0.0:
* IAM3 is now based on log4j v2.17.1, log4j 1.2 is no longer supported
* Runtime node is packaged as a par-file
* Toolkit node appears in the palette under Error handling
* Support for App Connect Enterprise V12.0.3.0

New in v1.2.4a
* Support for App Connect Enterprise V11.0.0.3.

New in v1.2.4
* Under heavy load there was a synchronization issue with loggers.

New in v1.2.3
* Node fails to log ExceptionList in combination with RAW, RAWLF, XML, XMLLF

New in v1.2.2
* Support for IBM Integration Bus V10.0.
* ESQL initLog4j now only returns true if initialization was successful.

New in v1.2.1b
* Support for IBM Integration Bus v9.0

New in v1.2.1
* Improving performance when handling big messages.
* Rework on the XMLLF output style.
* LoggerName and LogLevel can be set by using LocalEnviroment.
* LocalEnvironment supported in LogText.

Fixed in v1.2.1:
* Node fails to log Environment and LocalEnvironment values correctly.

## Details
Author: Matthias Nieder, IBM Consulting, IBM Germany

Category: 2

Released: 18Nov08

Last updated: 23Jan23

Current SupportPac Version: 2.0.1

## Prerequisites
This SupportPac requires:
* IBM App Connect Enterprise V11.0.0.3 or higher
* IBM App Connect Enterprise V12.0.3.0 or higher

## Download Instruction
Go to https://github.com/ot4i/node-for-log4j/releases and download the latest release or click on the release you want to download on the right pane.

In the Source.zip you will find the User's Guide iam3.pdf.

Download the Log4jLoggingNode par-file and install it as described in the User's Guide.

Download the Log4jLoggingPluginFeature zip-file and install the plugin into the toolkit as described in the User's Guide.

## Installation Instructions
To install this SupportPac:
1. Download the files from the release page.
2. Extract the source zip file and follow the instructions in the User’s guide IAM3.pdf.

If you encounter problems after upgrading the WebSphere Message Broker Toolkit to a new version:
1. Look into $TOOLKIT_INSTALL_DIR\configuration\org.eclipse.update.
2. Save a version of the file platform.xml.
3. Edit the file platform.xml as follows:

Replace the line:

`<site enabled="true" policy="USER-EXCLUDE" updateable="true" list="Log4jLoggingPlugin/" url="platform:/base/">`

with:

`<site enabled="true" policy="USER-EXCLUDE" updateable="true" url="platform:/base/">`

4. Restart the toolkit with the -clean option.

## Technical Support
Category 2 SupportPacs are provided in good faith and AS-IS. There is no warranty or further service implied or committed and any supplied sample code is not supported via IBM product service channels.

Please read the license information contained within this SupportPac to determine if you want to use it.
