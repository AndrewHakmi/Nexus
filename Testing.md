# Testing AutoGPT

We appreciate your interest in testing AutoGPT! Your contribution is very valuable and can help ensure we ship better software.

Testing is available for all technical levels. You do not need to be a programmer. Any user of AutoGPT can be a tester.  

Below are some tips to get you started.

## Communication: Discord Testing Channels

First, we recommend joining our testing community on Discord, where most of our communication occurs. To join, click on the `#testing` channel.

In this Discord, you can choose a role (or multiple roles) based on the platform you'll be testing on. To do this, use the following emoji to alert a moderator to give you the appropriate role:

- :apple: for MacOS Tester
- :penguin: for Linux Tester
- :computer: for Windows Tester
- :whale: for Docker Tester

If there are new testing roles you'd like to see added, let us know!

You'll receive updates and information relevant to your platform with the correct role.

## Testing a Pull Request

Oftentimes, you're testing software that's not been released yet. You will want to be familiar with accessing the main version or the latest released version of the software to compare the before and after scenarios. For the main installation instructions, see here: https://github.com/Significant-Gravitas/Auto-GPT/blob/master/README.md

Once you know how to use the official version of AutoGPT, testing is very similar - except that you're most likely downloading a pull request. 

How do you get this pull request? - well, it most likely will have been posted in the #testing Discord channel.

Here's a simple guide on how to access a pull request and clone it to your computer:

1. Use a 👍 or ✅ to notify others that you're testing. This helps the poster know that someone's on it and also helps prevent too many people from testing the same thing.
1. Navigate to the repository's [main page on GitHub](https://github.com/Significant-Gravitas/Auto-GPT/).
2. Instead of downloading the main version, Click on the "Pull requests" tab at the top.
3. Select the pull request you're interested in.
4. Under the "Code" dropdown, click the "Download ZIP" option.
5. Once downloaded, unzip the file in your chosen directory. It's preferable to keep it separate from your main AutoGPT installation. That way, you can do side-by-side comparisons.
6. Open this directory in your terminal and run your tests.

For those who are familiar with Git, you can use the following commands to clone and checkout the branch related to the pull request:

```bash
git clone https://github.com/username/repository.git
cd repository
git checkout branch-name
```

Remember to replace "username," "repository," and "branch-name" with the appropriate values.

## What to Test

There are whole books and websites dedicated to testing, but for those who'd like a guide, you'll want to perform two types of tests.
1. Does the PR meet its goal? 
- Read the PR description, and test the specific features it's supposed to address.
- Start by trying to replicate the bug/issue that the PR addresses. Can you replicate it?
- If you can replicate it, please note down the steps you took to reproduce it.
- If you cannot replicate it, is it now fixed precisely how the PR describes?

1. Does it break anything that works fine in the latest stable version? Start with AutoGPT's main flows:
- Can you still name your AI, enter a role, set a simple goal, and run it to completion? 
- Can you still do the automatic path that doesn't require entering any goals?
- A two-step goal is sufficient. 
- A good starter test is to see if AutoGPT can write its name to a file called name.txt

## Reporting Your Test Results

Once you've run your tests, it's time to report the results. Here's how you can do this:

1. Go back to the pull request page on GitHub.
2. Scroll down to the "Leave a comment" text box.
3. Provide a clear and concise description of your test and its results. Mention any bugs or issues you encountered.
4. Click the "Comment" button.

Please, keep track of all the tests you perform in a document (e.g., Google Docs, Word). That'll help you remember the results so that the maintainers can understand the context and conditions of each test.

## Other Important Topics

1. **Bug Reporting**: If you find a bug, please create an issue on the GitHub repository detailing the bug and how you found it. Be sure to label the issue as a 'bug.'

2. **Test Coverage**: Cover as much functionality as possible. Users use software differently, and your unique usage could uncover important issues.

3. **Communication**: Always feel free to ask questions and share ideas on the `#testing` Discord channel. We're here to help!

Thank you for your contribution! Your efforts help make our software better. Happy testing!