<!---
 Licensed to the Apache Software Foundation (ASF) under one or more
 contributor license agreements.  See the NOTICE file distributed with
 this work for additional information regarding copyright ownership.
 The ASF licenses this file to You under the Apache License, Version 2.0
 (the "License"); you may not use this file except in compliance with
 the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
-->
<!---
 +======================================================================+
 |****                                                              ****|
 |****      THIS FILE IS GENERATED BY THE COMMONS BUILD PLUGIN      ****|
 |****                    DO NOT EDIT DIRECTLY                      ****|
 |****                                                              ****|
 +======================================================================+
 | TEMPLATE FILE: readme-md-template.md                                 |
 | commons-build-plugin/trunk/src/main/resources/commons-xdoc-templates |
 +======================================================================+
 |                                                                      |
 | 1) Re-generate using: mvn commons-build:readme-md                    |
 |                                                                      |
 | 2) Set the following properties in the component's pom:              |
 |    - commons.componentid (required, alphabetic, lower case)          |
 |    - commons.release.version (required)                              |
 |                                                                      |
 | 3) Example Properties                                                |
 |                                                                      |
 |  <properties>                                                        |
 |    <commons.componentid>math</commons.componentid>                   |
 |    <commons.release.version>1.2</commons.release.version>            |
 |  </properties>                                                       |
 |                                                                      |
 +======================================================================+
--->
Apache Commons Crypto
===================

[![Java CI](https://github.com/apache/commons-crypto/actions/workflows/maven.yml/badge.svg)](https://github.com/apache/commons-crypto/actions/workflows/maven.yml)
[![Coverage Status](https://codecov.io/gh/apache/commons-crypto/branch/master/graph/badge.svg)](https://app.codecov.io/gh/apache/commons-crypto)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.commons/commons-crypto/badge.svg?gav=true)](https://maven-badges.herokuapp.com/maven-central/org.apache.commons/commons-crypto/?gav=true)
[![Javadocs](https://javadoc.io/badge/org.apache.commons/commons-crypto/1.2.0.svg)](https://javadoc.io/doc/org.apache.commons/commons-crypto/1.2.0)
[![CodeQL](https://github.com/apache/commons-crypto/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/apache/commons-crypto/actions/workflows/codeql-analysis.yml)
[![OpenSSF Scorecard](https://api.securityscorecards.dev/projects/github.com/apache/commons-crypto/badge)](https://api.securityscorecards.dev/projects/github.com/apache/commons-crypto)

Apache Commons Crypto is a cryptographic library optimized with AES-NI (Advanced Encryption
Standard New Instructions). It provides Java API for both cipher level and Java stream level.
Developers can use it to implement high performance AES encryption/decryption with the minimum
code and effort. Please note that Crypto doesn't implement the cryptographic algorithm such as
AES directly. It wraps to OpenSSL or JCE which implement the algorithms.

Features
--------

1. Cipher API for low level cryptographic operations.
2. Java stream API (CryptoInputStream/CryptoOutputStream) for high level stream encryption/decryption.
3. Both optimized with high performance AES encryption/decryption. (1400 MB/s - 1700 MB/s throughput in modern Xeon processors).
4. JNI-based implementation to achieve comparable performance to the native C/C++ version based on OpenSsl.
5. Portable across various operating systems (currently only Linux/MacOSX/Windows);
   Apache Commons Crypto loads the library according to your machine environment (it checks system properties, `os.name` and `os.arch`).
6. Simple usage. Add the commons-crypto-(version).jar file to your classpath.


Export restrictions
-------------------

This distribution includes cryptographic software.
The country in which you currently reside may have restrictions
on the import, possession, use, and/or re-export to another country,
of encryption software. BEFORE using any encryption software,
please check your country's laws, regulations and policies
concerning the import, possession, or use, and re-export of
encryption software, to see if this is permitted.
See <http://www.wassenaar.org/> for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS),
has classified this software as Export Commodity Control Number (ECCN) 5D002.C.1,
which includes information security software using or performing
cryptographic functions with asymmetric algorithms.
The form and manner of this Apache Software Foundation distribution makes
it eligible for export under the License Exception
ENC Technology Software Unrestricted (TSU) exception
(see the BIS Export Administration Regulations, Section 740.13)
for both object code and source code.

The following provides more details on the included cryptographic software:

* Commons Crypto use [Java Cryptography Extension](http://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html) provided by Java
* Commons Crypto link to and use [OpenSSL](https://www.openssl.org/) ciphers

Documentation
-------------

More information can be found on the [Apache Commons Crypto homepage](https://commons.apache.org/proper/commons-crypto).
The [Javadoc](https://commons.apache.org/proper/commons-crypto/apidocs) can be browsed.
Questions related to the usage of Apache Commons Crypto should be posted to the [user mailing list][ml].

Where can I get the latest release?
-----------------------------------
You can download source and binaries from our [download page](https://commons.apache.org/proper/commons-crypto/download_crypto.cgi).

Alternatively, you can pull it from the central Maven repositories:

```xml
<dependency>
  <groupId>org.apache.commons</groupId>
  <artifactId>commons-crypto</artifactId>
  <version>1.2.0</version>
</dependency>
```

Contributing
------------

We accept Pull Requests via GitHub. The [developer mailing list](https://commons.apache.org/mail-lists.html) is the main channel of communication for contributors.
There are some guidelines which will make applying PRs easier for us:
+ No tabs! Please use spaces for indentation.
+ Respect the code style.
+ Create minimal diffs - disable on save actions like reformat source code or organize imports. If you feel the source code should be reformatted create a separate PR for this change.
+ Provide JUnit tests for your changes and make sure your changes don't break any existing tests by running ```mvn```.

If you plan to contribute on a regular basis, please consider filing a [contributor license agreement](https://www.apache.org/licenses/#clas).
You can learn more about contributing via GitHub in our [contribution guidelines](CONTRIBUTING.md).

License
-------
This code is under the [Apache License v2](https://www.apache.org/licenses/LICENSE-2.0).

See the `NOTICE.txt` file for required notices and attributions.

Donations
---------
You like Apache Commons Crypto? Then [donate back to the ASF](https://www.apache.org/foundation/contributing.html) to support the development.

Additional Resources
--------------------

+ [Apache Commons Homepage](https://commons.apache.org/)
+ [Apache Issue Tracker (JIRA)](https://issues.apache.org/jira/browse/CRYPTO)
+ [Apache Commons Slack Channel](https://the-asf.slack.com/archives/C60NVB8AD)

Apache Commons Components
-------------------------

Please see the [list of components](https://commons.apache.org/components.html)
