## This is the newly created Frequently Asked Questions page
This page contains solutions to a lot of common issues and errors, try to find your problem here before posting on discord or filing an issue on github.


## Common Questions:

<details>
  <summary>Where does Auto-GPT save the files it creates?</summary>
  If you have not changed anything to the workspace variables, Auto-GPT saves its files in "Path_to_Auto-GPT...\Auto_GPT\autogpt\Auto-GPT-workspace"
</details>

<details>
  <summary>I have a paid chatGPT account, why does my Auto-GPT not work?</summary>
  A paid openAI chatGPT account is not the same as an openAI API account. Go to <a href="platform.openai.com">OpenAI Platform</a> and make sure you have a valid billing method set.
</details>

<details>
  <summary>I changed my <b>.env</b> file and saved it, but why does Auto-GPT still not work?</summary>
  Double check your<b>.env</b> file and make sure that the lines you are using do not contain a <b>#</b> and a space at the beginning of the line.
</details>


## Common Issues:

<details>
  <summary>Auto-GPT does not see the file it created:</summary>
  Enable the view file extensions option in your OS.
</details>

<details>
  <summary>Why does the Auto-GPT say that I don't have my OpenAI key set?</summary>
  Please double check that you have set your OpenAI API Key correctly in the <b>.env</b> file, and not the <b>.env.template</b> file.
</details>


## Common Error Messages:

<details>
  <summary>openai.error.InvalidRequestError: The model: gpt-4 does not exist:</summary>
  You do not have api access to GPT-4. Set your smart_LLM_model to gpt-3.5-turbo and your token_limit to 4000
</details> 

<details>
  <summary>ImportError DLL load failed while importing:</summary>
  Make sure you have the latest <a href="https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#visual-studio-2015-2017-2019-and-2022">Microsoft Visual C++ Redistributable</a> installed.
</details>

<details>
  <summary>Command write_to_file returned: Error: 'PosixPath' object has no attribute 'is_relative_to':</summary>
  Your python version is not recent enough. Update to Python 3.10.
</details>

<details>
  <summary>This model's maximum context length is "X" tokens, however you requested "larger_than_X tokens":</summary>
  Check that BROWSE_CHUNK_MAX_LENGTH is set correctly in the .env file. The default is 3000.
<details>