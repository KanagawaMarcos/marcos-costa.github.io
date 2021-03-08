
- centralize deployment
-- Its part manual part automatic
-- We dont know works production.
-- 1. Open MR to change the image tag for the service. (serial number).
-- 2. manually create an new image with the new tag in the MR.
-- error: you won't have the old stuff running, and you env breaks.
--- fix: revert the commit and it will re run the script and the old stuff will be there.

-- Automate: build image process.
-- automate: Merge Request.
-- Automate: add a service to centralized services.

-- Stage tag = builds a docker image in GI registry (palantir).
--- You can replicate it and just do via request a new tag.
-- centralized has registry read access to the registry.


-------------DS Deployment-------------

-1. Create a docker file
- builds an image
- push the image to the registry.
0. Create a gitlab access key (read_registry).
1. You create a ec2 instance.
2. Connect to the docker regristry 
-- docker login registry.gitlab.com
3. docker pull. 
4. docker container run --restart always.
- docker container run --rm -ir registry.gitlab.

