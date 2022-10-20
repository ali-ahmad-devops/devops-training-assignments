# How to leverage cache using Dockerfiles:
Leveraging your cache involves layering your images so that only the bottom layers change often.
You want your RUN steps that change more frequently towards the bottom of the Dockerfile, while steps that change less often should be ordered towards the top