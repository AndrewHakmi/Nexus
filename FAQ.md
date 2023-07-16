## This is the newly created Frequently Asked Questions page

This page contains solutions to common issues and errors, try to find your problem here before posting on discord or
filing an issue on github. If you have a solution to an issue not mentioned here, please post these in *
*[Common issues](https://discord.com/channels/1092243196446249134/1109907151419347044)** discord channel.

> NOTE: For information on how to install or setup Auto-GPT revert to the **[docs](https://docs.agpt.co/)**

## Common Questions:

<details>
  <summary>Where does Auto-GPT save the files it creates?</summary>
  If you have not changed anything to the workspace variables, Auto-GPT saves its files to:<br><b>linux</b> : ..\Auto-GPT\autogpt\auto_gpt_workspace<br><b>windows</b> : ..\Auto-GPT\autogpt\auto_gpt_workspace<br><b>Mac</b> : ..\Auto-GPT\autogpt\auto_gpt_workspace
</details>

<details>
  <summary>How do i start Auto-GPT?</summary>
  A full description for this is given in the <a href="https://docs.agpt.co/setup/"><b>docs</b></a>
</details>

<details>
  <summary>I have a paid chatGPT account, why does my Auto-GPT not work?</summary>
  A paid openAI chatGPT account is not the same as an openAI API account. Go to <a href="platform.openai.com"><b>OpenAI Platform</b></a> and make sure you have a valid billing method set. You will likely also want to join the gpt 4 waitlist which can be done <a href="https://openai.com/waitlist/gpt-4-api"><b>here</b></a>
</details>

<details>
  <summary>I want to setup Auto-GPT, but i cannot find the dependencies</summary>
  In the Auto-GPT main folder run the following command:<br>"pip install -r requirements.txt".
</details>

<details>
  <summary>I changed my <b>.env</b> file and saved it, but why does Auto-GPT still not work?</summary>
  Double check your<b>.env</b> file and make sure that the lines you are using do not contain a <b>#</b> and a 
  space at the beginning of the line. It should look like this :<br>
  #########<br>
  ### LLM PROVIDER<br>
  #########<br>
  OPENAI_API_KEY=your-key-here-no-quotes<br>
  TEMPERATURE=.2<br>
  # USE_AZURE=False<br>
  ### AZURE<br>
  # moved to azure.yaml.template<br>
</details>

## Common Issues:

<details>
  <summary>Auto-GPT does not see the file it created:</summary>
  Enable the view file extensions option in your OS.
</details>

<details>
  <summary>Why does the Auto-GPT say that I don't have my OpenAI key set?</summary>
  Please double check that you have set your OpenAI API Key correctly in the <b>.env</b> file, and not the 
  <b>.env.template</b> file. It should look similar to this:<br>
  ####<br>
  ### LLM PROVIDER<br>
  ####<br>
  OPENAI_API_KEY=your-key-here-no-quotes<br>
  TEMPERATURE=.2<br>
  # USE_AZURE=False<br>
</details>

<details>
  <summary>python -m autogpt does not work:</summary>
  Use the following command in your Auto-GPT folder:<br>
  <b>Mac:</b> ./run.sh <br>
  <b>Windows:</b> .\run.bat<br>
</details>

<details>
  <summary>How do i update Auto-GPT using Docker?</summary>
  Use the command: "docker pull significantgravitas/auto-gpt:latest" in your container.
</details>

<details>
  <summary>How do i update Auto-GPT using Git?</summary>
  Use the command: "git pull origin master" in the main Auto-GPT folder.
</details>

## Common Error Messages:

<details>
  <summary>openai.error.InvalidRequestError: The model: gpt-4 does not exist:</summary>
  You do not have api access to GPT-4. Set your smart_LLM to gpt-3.5-turbo and your token_limit to 4000. 
  Also you will need to join the gpt4 waitlist here : https://openai.com/waitlist/gpt-4-api. Your <b>.env</b> 
  should look like:<br>
  ####<br>
  ### LLM MODELS<br>
  ####<br>
  <br>
  ## SMART_LLM - Smart language model (Default: gpt-4)<br>
  ## FAST_LLM - Fast language model (Default: gpt-3.5-turbo)<br>
  SMART_LLM=gpt-3.5-turbo<br>
  FAST_LLM=gpt-3.5-turbo<br>
  <br>
  ### LLM MODEL SETTINGS<br>
  ## FAST_TOKEN_LIMIT - Fast token limit for OpenAI (Default: 4000)<br>
  ## SMART_TOKEN_LIMIT - Smart token limit for OpenAI (Default: 8000)<br>
  ## When using --gpt3only this needs to be set to 4000.<br>
  FAST_TOKEN_LIMIT=4000<br>
  SMART_TOKEN_LIMIT=4000<br>
</details> 

<details>
  <summary>ImportError DLL load failed while importing:</summary>
  Make sure you have the latest <a href="https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc- 
 redist?view=msvc-170#visual-studio-2015-2017-2019-and-2022">Microsoft Visual C++ Redistributable</a> 
  installed.
</details>

<details>
  <summary>NotImplementedError: The Redis memory backend has been rendered incompatible by work on the memory system, and has been removed temporarily.</summary>
  in your .env find the section on memory, there find the following variables: MEMORY_BACKEND and MEMORY_INDEX. set MEMORY_BACKEND to "json_file" and remove the hashtag and space in front of both variables.
</details>

<details>
  <summary>Command write_to_file returned: Error: 'PosixPath' object has no attribute 'is_relative_to': </summary>
  Your python version is not recent enough. Update to Python 3.10. You may also need to take the old python out 
  of your PATH. How this is done depends on the OS you're using and can vary by preference. Look for 
  information on your specific OS and version.</details>

<details>
  <summary>This model's maximum context length is "X" tokens, however you requested "larger_than_X tokens":</summary>
  Check that BROWSE_CHUNK_MAX_LENGTH is set correctly in the .env file. The default is 3000. Set it lower if 
  you are having the error persist.<br>
  This is an example of how the section of the .env should look :<br>
  ####<br>
  ### WEB BROWSING<br>
  ####<br>
  <br>
  ### BROWSER<br>
  ## HEADLESS_BROWSER - Whether to run the browser in headless mode (default: True)<br>
  ## USE_WEB_BROWSER - Sets the web-browser driver to use with selenium (default: chrome).<br>
  ##   Note: set this to either 'chrome', 'firefox', 'safari' or 'edge' depending on your current browser<br>
  HEADLESS_BROWSER=False<br>
  USE_WEB_BROWSER=firefox<br>
  ## BROWSE_CHUNK_MAX_LENGTH - When browsing website, define the length of chunks to summarize (in number of 
  tokens, excluding the response. 75 % of # FAST_TOKEN_LIMIT is usually wise )<br>
  BROWSE_CHUNK_MAX_LENGTH=2000<br>
  ## BROWSE_SPACY_LANGUAGE_MODEL is used to split sentences. Install additional languages via pip, and set the 
  model name here.<br> 
  Example Chinese: 
  # python -m spacy download zh_core_web_sm<br>
  BROWSE_SPACY_LANGUAGE_MODEL=en_core_web_sm
</details>
