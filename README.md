# FillTheForm

[![Build Status](https://travis-ci.org/Hotel-Reservation-Service/FillTheForm.svg?branch=master)](https://travis-ci.org/Hotel-Reservation-Service/FillTheForm)
[![License](https://img.shields.io/badge/license-Apache%202-green.svg?style=flat)](https://github.com/Hotel-Reservation-Service/FillTheForm/blob/master/LICENSE)

FillTheForm is an Android app that that helps you to develop and test apps faster.

Now you can fill out every EditText with just a long press!

## FillTheForm Speed Test ##
[![FillTheForm Speed Test](http://i.imgur.com/w3Ic0H9.png)](https://youtu.be/99MNtYpOUlk "FillTheForm Speed Test")

## Requirements
* Android 5+
* FillTheFormSample app or your Android app with EditText elements that have id-s

## Usage
* Import this project to Android Studio
* Install FillTheFormSample app
* Install FillTheForm app
* Open FillTheForm app. Enable all required permissions and then press 'Load configuration'
* Press the button 'com.hrs.filltheformsample'
* Long press one of the EditText fields in the FillTheFormSample app

## Create configuration file for your Android app

Single item in the configuration file should have the following format:
```xml
<edit_text_id>value</edit_text_id>
```


Items can be grouped in profiles:
```xml
<profile name="Profile name">
    ...
    <edit_text_id>value</edit_text_id>
    <other_edit_text_id>other_value</other_edit_text_id>
    ...
</profile>
```


This is the configuration file for the FillTheFormSample app:

```xml
<fillTheFormConfig>
    <packages>
        <package>com.hrs.filltheformsample</package>
        <package>com.hrs.filltheformsampletwo</package>
    </packages>
    <profiles>
        <profile name="Max Mustermann Profile">
            <first_name>Max</first_name>
            <last_name>Mustermann</last_name>
            <email>max.mustermann@mustermann.de</email>
            <city>Köln</city>
            <city>Düsseldorf</city>
            <state>NRW</state>
            <country>Germany</country>
            <country>Deutschland</country>
            <phone>+491234879625</phone>
            <zip_code>50667</zip_code>
            <comment>Viele Grüße aus NRW!</comment>
        </profile>
        <profile name="John Doe Profile">
            <first_name>John</first_name>
            <last_name>Doe</last_name>
            <email>john.doe@johndoe.com</email>
            <email>doe@johndoe.com</email>
            <city>San Francisco</city>
            <state>California</state>
            <country>United States of America</country>
            <country>USA</country>
            <phone>(415) 321-654</phone>
            <zip_code>CA 94129</zip_code>
            <comment>Welcome to San Francisco!</comment>
        </profile>
        <profile name="Random Test Profile">
            <first_name>random_first_name</first_name>
            <last_name>random_last_name</last_name>
            <email>random_email</email>
            <city>random_city</city>
            <state>random_state</state>
            <country>random_country</country>
            <phone>random_phone</phone>
            <zip_code>random_zip_code</zip_code>
            <comment>random_text</comment>
            <comment>random_paragraph</comment>
        </profile>
    </profiles>
    <!-- No profile -->
    <first_name>Ivan</first_name>
    <last_name>Jukic</last_name>
    <country>Croatia</country>
    <city>Imotski</city>
</fillTheFormConfig>
```

## License

FillTheForm is available under the Apache 2 license. See the LICENSE file for more info.