# HOW-OneLiner

## What is this?

Generate a one-liner command for what you would like to do with ChatGPT.

## Requirements

- OpenAI API Key. Get from [here](https://platform.openai.com/signup/)

## How this work?

The command is generated in the following steps.

1. Translate the input in any language into English
2. Generates commands based on the translated
3. Up to 3 candidates will be generated.

Example:

```console
### Set OpenAI API Key
$ export OAI_API_KEY=xxxxxxx

### English
$ how-oneliner Output a list of files that have been modified within the last hour in the current directory.

OR

### Other language
$ how-oneliner 現在のディレクトリ内で１時間以内に変更されたファイル一覧を出力
```

Outputs

```console
$ find . -maxdepth 1 -type f -mmin -60
$ find . -maxdepth 1 -type f -mmin -60 -print
$ find . -maxdepth 1 -type f -mmin -60 -print 2>/dev/null
```
