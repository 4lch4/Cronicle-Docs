# Cronicle Documentation

This website is a "fan-made" documentation site for the [Cronicle Service][0] created by [Jhuckaby][1]. I created this website because the [original documentation][2] is a single README file that can be rather difficult to consume. The content on this site is directly from that original README, but in a different format.

For the full original documentation, visit the [Cronicle repo][0] and view the [README][2].

## Upgrading Multi-Server Clusters From v0.8 to v0.9

For those upgrading multi-server clusters from Cronicle v0.8 to v0.9, you must upgrade **all** of your servers for them to be able to communicate. In v0.9 we have upgraded to socket.io v4.4, which is incompatible with socket.io v1.7.3 that previous Cronicle versions used. We had to upgrade this dependency due to high severity vulnerabilities. Since this is a breaking API change for them, you cannot run "mixed" server clusters with some servers on Cronicle v0.8 and others on v0.9. They all have to be on v0.8 or they all have to be on v0.9.

So, it is recommended that you first disable the main scheduler on your master server (checkbox in top-right corner of the UI), wait for all jobs to complete, then shut down all servers and upgrade them all together. Then start them all up again, and finally re-enable the scheduler.

[0]: https://github.com/jhuckaby/Cronicle/
[1]: https://github.com/jhuckaby
[2]: https://github.com/jhuckaby/Cronicle/#readme
