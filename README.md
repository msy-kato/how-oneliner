# How-OneLiner

## What is this?

Generate a one-liner command for what you would like to do with ChatGPT.

## Requirements

- Get OpenAI API Key from [here](https://platform.openai.com/signup/).
- `curl` command

## How this work?

The command is generated in the following steps.

1. Translate the input in any language into English
2. Generates commands based on the translated
3. Up to 3 candidates will be generated.

Example:

```console
### English
$ how-oneliner Output a list of files that have been modified within the last hour in the current directory.

-- OR --

### Other language
$ how-oneliner 現在のディレクトリ内で１時間以内に変更されたファイル一覧を出力
```

Outputs

```console
$ find . -maxdepth 1 -type f -mmin -60
$ find . -maxdepth 1 -type f -mmin -60 -print
$ find . -maxdepth 1 -type f -mmin -60 -print 2>/dev/null
```

## Quick start

Setup.

```console
$ curl -s https://raw.githubusercontent.com/msy-kato/how-oneliner/main/how-oneliner -o /path/to/bin/how-oneliner
$ chmod u+x /path/to/bin/how-oneliner
```

How to execute.

```console
$ export OAI_API_KEY=xxxxxxx
$ how-oneliner Output a list of files that have been modified within the last hour in the current directory.
$ how-oneliner Calculate the sum of the products of columns 2 and 3 of the standard input
$ how-oneliner 東京の明日の天気を確認
```

Help.

```console
$ how-oneliner -h
```
