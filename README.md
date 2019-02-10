## Setup
Install OpenJDK 8
```
$ sudo apt install openjdk-8-jdk
```
Verify that this is installed with
```
$ java -version
```
```
Output
openjdk version "1.8.0_162"
OpenJDK Runtime Environment (build 1.8.0_162-8u162-b12-1-b12)
OpenJDK 64-Bit Server VM (build 25.162-b12, mixed mode)
```


Install Maven 
```
$ sudo apt update
$ sudo apt install maven
```
Verify the installation by running the mvn -version command:
```
$mvn -version
```
```
Output : 
Apache Maven 3.5.2
Maven home: /usr/share/maven
Java version: 1.8.0_191, vendor: Oracle Corporation
Java home: /usr/lib/jvm/java-8-openjdk-amd64/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "4.15.0-29-generic", arch: "amd64", family: "unix"
```

## Usage

Inside the ​ parking_lot​ directory, execute with this command to compile source code
```
$ ./bin/setup
```

There are 2 ways to launch apps,
1. Include file_input.txt as scenario, please execute this command :
```
$ ./bin/parking_lot file_input.txt
```
2. Interactive scenario, please execute this command :
```
$ ./bin/parking_lot
```
Example interactive scenario :
```
$ create_parking_lot 3

Created a parking lot with 3 slots

$ park KA-01-HH-1234 White

Allocated slot number:1

$ park KA-01-HH-9999 White

Allocated slot number:2

$ park KA-01-BB-0001 Black

Allocated slot number:3

$ leave 2

Slot number 2 is free

$ status

Slot No. Registration No. Colour
1	KA-01-HH-1234	White
3	KA-01-BB-0001	Black

$ park KA-01-P-333 White

Allocated slot number:2

$ park DL-12-AA-9999 White

Sorry, parking lot is full

$ registration_numbers_for_cars_with_colour White

KA-01-HH-1234,KA-01-P-333

$ slot_numbers_for_cars_with_colour White

1,2

$ slot_number_for_registration_number KA-01-BB-0001

3

$ slot_number_for_registration_number MH-04-AY-1111

Not found

$ exit
```
