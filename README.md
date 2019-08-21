# Phase2 - Docker in Docker

We ran into an issue recently where all our projects relied on the public `docker:dind` image, but an update to that image caused all project builds to fail.

To mitigate this possibility in the future, this repo will simply extend the latest stable tag on the public `docker:stable-dind` image with no material changes. This will allow all our projects to point to a single `outrigger/dind:stable` that we will update as new releases of the public `docker:stable-dind` image are published. Though it is unlikely we will run into the same problem, it is important that we be capable of reverting to using an older stable image tag for all projects quickly as needed.
