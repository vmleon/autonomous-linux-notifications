# Autonomous Linux and Oracle Notification Service

Getting started with Oracle Autonomous Linux distribution and how to configure to get kernel updates notifications by email.

Oracle Linux executes autonmatic path updates and tinung with human interaction.

## Create Notification topic

Create a notification topic

Go to Application Integration > Notification

```
Allow dynamic-group <dynamic-group-name> to use ons-topic in compartment <compartment-name> where request.permission='ONS_TOPIC_PUBLISH'
```

## Configure instances for Notification

Identity > Dynamic Groups

```
ALL {instance.compartment.id = '<Compartment_OCID>'}
```

## Create an Autonomous Linux

XXX

```
#!/bin/bash
al-config -T <ONS_TOPIC_OCID>
```

Connect to your Linux

```
ssh –i id_rsa opc@<Public_IP_Address>
```

Check oci-metadata

```
sudo oci-metadata
```
