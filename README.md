# first-exercises
what is isolatiion in docker=
Containers offer a standardized format in which to package software and isolate their runtime from the rest of the host operating system. Essentially, they represent a lighter-weight alternative to traditional virtual machines because they do not require embedding a complete OS to execute an application.

the diffrense between cmd and entrypoint = 

cmd = 
You can set default commands with parameters using the CMD instruction. If you run a Docker container without specifying any additional CLI commands, the CMD instruction will be executed. You can include an executable as the default command. However, if you choose to omit it, you will have to specify an ENTRYPOINT instruction along with the CMD instruction
If you have specified an argument along with the Docker run command, the default one specified using the CMD instruction will be ignored. Also, if you have specified multiple CMD instructions inside a single dockerfile, the one specified at the last will only be executed.

intrypoint = 
The ENTRYPOINT instruction looks almost similar to the CMD instruction. However, the main highlighting difference between them is that it will not ignore any of the parameters that you have specified in the Docker run command (CLI parameters).
When we have specified the ENTRYPOINT instruction in the executable form, it allows us to set or define some additional arguments/parameters using the CMD instruction in Dockerfile. If we have used it in the shell form, it will ignore any of the CMD parameters or even any CLI arguments.

diffrence between arg and env = 

ARG and env can be confusing at first. Both are Dockerfile instructions which help you define variables, and from within the Dockerfile they feel pretty similar.
ENV is for future running containers. ARG for building your Docker image.

ENV is mainly meant to provide default values for your future environment variables. Running dockerized applications can access environment variables. It’s a great way to pass configuration values to your project and You can’t change ENV directly during the build.
ARG values are not available after the image is built. A running container won’t have access to an ARG variable value But unlike ARG, you can’t override ENV values directly from the commandline when building your image. However, you can use ARG values to dynamically set default values of ENV variables during the build.


ARG and ENV overlap during the image build. This causes confusion sometimes: from within your Dockerfile, both ARG and ENV seem very similar. Both can be accessed from within your Dockerfile commands in the same manner.


