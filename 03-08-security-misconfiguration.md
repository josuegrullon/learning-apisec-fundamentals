

#### API8: Security Misconfiguration
- Missing security patches
- Missing TLS/ SSL etc

All right. #8 on the OWASP API Security Top 10 is Security Misconfiguration.

 This is a pretty broad category that basically encompasses. All kinds of vulnerabilities that can result from misconfiguration, whether it's on the servers, the infrastructure the network, the application themselves.

It's looking for things that, these are vulnerabilities that bots and scanners often are looking for. It could be unpatched systems or services that shouldn't be running. The exposure here could be anything from lack of or a loss of data to full server compromise. So examples are a lack of hardening or, we're not properly hardening OSes and applications, we're not setting permissions properly for the applications for the cloud services that they use, and the like. Missing security patches on libraries and applications used within our service. Unnecessary features enabled, no need to have SFTP enabled on a server if that's not a requirement for the application to run. Missing encryption, transport layer security.

CORS, Cross Origin Resource Sharing. You want to make sure that your APIs can only be accessed by properly identified and approved sources. So if you've got missing CORS policies, that's another potential source of a vulnerability.

The prevention side, of course, implement proper hardening procedures across the entire stack. Review those procedures and test to verify that all the infrastructure that you're running is properly secured and up to date.