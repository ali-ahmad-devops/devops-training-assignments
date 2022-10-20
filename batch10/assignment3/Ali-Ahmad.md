# How to leverage cache using Dockerfiles:
Leveraging your cache involves layering your images so that only the bottom layers change often.
You want your RUN steps that change more frequently towards the bottom of the Dockerfile, while steps that change less often should be ordered towards the top
#  What are multi-stage builds:
With multi-stage builds, you use multiple FROM statements in your Dockerfile. Each FROM instruction can use a different base, and each of them begins a new stage of the build. You can selectively copy artifacts from one stage to another, leaving behind everything you don't want in the final image.