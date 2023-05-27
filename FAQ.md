## This is the newly created Frequently Asked Questions page
This page contains solutions to a lot of common issues and errors, try to find your problem here before posting on discord or filing an issue on github.

## Common Issues:

<details>
  <summary>Auto-GPT is not seeing a file:</summary>
  Enable the view file extensions option in your OS.
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