## Congratulations, 
you almost made your first step to becoming an AI-whisperer. Depending on the istallation you have chosen, you can find the information on how to run your auto-GPT for the first time below:

> We all like to dive in, but this is an advanced alien spacecraft 🚁. 
> Luckily our core-devs have provided a manual! Remember to check the docs folder in your installation for even more guidance 

# With Docker:

Easiest is to use docker-compose.

**Important: Docker Compose version 1.29.0 or later is required to use version 3.9 of the Compose file format.** You can check the version of Docker Compose installed on your system by running the following command:

docker-compose version

This will display the version of Docker Compose that is currently installed on your system.

If you need to upgrade Docker Compose to a newer version, you can follow the installation instructions in the Docker documentation: https://docs.docker.com/compose/install/

Once you have a recent version of docker-compose, run the commands below in your Auto-GPT folder.

### Build the image: 
If you have pulled the image from Docker Hub, skip this step (NOTE: You will need to do this if you are modifying requirements.txt to add/remove depedencies like Python libs/frameworks)

```shell
docker-compose build auto-gpt
```


### Run Auto-GPT:

```shell
docker-compose run --rm auto-gpt
```

By default, this will also start and attach a Redis memory backend. If you do not want this, comment or remove the depends: - redis and redis: sections from docker-compose.yml.

For related settings, see [Memory > Redis setup](https://github.com/Significant-Gravitas/Auto-GPT/blob/master/docs/configuration/memory.md#redis-setup).

You can pass extra arguments, e.g. running with --gpt3only and --continuous:

docker-compose run --rm auto-gpt --gpt3only --continuous


# In a dev-container:

> Install the [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension in VS Code.

> Open command palette with ++f1++ and type Dev Containers: Open Folder in Container.

> Run ./run.sh.


# Without Docker:

Create a virtual environment to run in.

```python 
python -m venv venvAutoGPT
source venvAutoGPT/bin/activate
pip3 install --upgrade pip
```

**!!! warning Due to security reasons, certain features (like Python execution) will by default be disabled when running without docker. So, even if you want to run the program outside a docker container, you currently still need docker to actually run scripts !!!**

Simply run the startup script in your terminal. This will install any necessary Python packages and launch Auto-GPT.

### On Linux/MacOS:

```shell
./run.sh
```

### On Windows:

```shell
.\run.bat
```

<pre>
</pre>
If this gives errors, make sure you have a compatible Python version installed. See also the [requirements](https://github.com/Significant-Gravitas/Auto-GPT/blob/master/docs/installation.md#requirements).
