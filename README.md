# aws-cdk
AWS CDK project

# Welcome to your CDK TypeScript project

This is a blank project for CDK development with TypeScript.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `npx cdk deploy`  deploy this stack to your default AWS account/region
* `npx cdk diff`    compare deployed stack with current state
* `npx cdk synth`   emits the synthesized CloudFormation template


```sh
cdk int app --language typescript
```

Check if it is ok with app deploy an application.
```sh
cdk synth 
```

Deploy the app
```sh
cdk deploy
```

Bootstrap enviroment if deploy fail in first atempted.
```sh
cdk bootstrap
`````````


Gotcha 👍 Here’s a **clean, practical AWS CDK command cheat sheet** — the stuff you actually use day-to-day.

---

## 🔧 Setup & Project Creation

### Install CDK

```bash
npm install -g aws-cdk
```

### Check version

```bash
cdk --version
```

### Create a new CDK app

```bash
cdk init app --language typescript
cdk init app --language python
cdk init app --language java
```

(Also supports `go`, `csharp`.)

---

## 🔐 AWS Environment

### Bootstrap an account (required once per account/region)

```bash
cdk bootstrap
```

Specific account/region:

```bash
cdk bootstrap aws://ACCOUNT_ID/REGION
```

Example:

```bash
cdk bootstrap aws://123456789012/us-east-1
```

---

## 📦 Dependency Management

### Add a CDK library

```bash
npm install aws-cdk-lib
npm install constructs
```

Python:

```bash
pip install aws-cdk-lib constructs
```

---

## 🧠 Understanding What Will Happen

### Synthesize CloudFormation

```bash
cdk synth
```

Outputs the generated CloudFormation template.

---

### See what will change (VERY important)

```bash
cdk diff
```

Shows:

* ➕ resources to be created
* 🔄 changes
* ❌ deletions

---

## 🚀 Deploying

### Deploy all stacks

```bash
cdk deploy
```

### Deploy a specific stack

```bash
cdk deploy MyStack
```

### Skip approval prompts

```bash
cdk deploy --require-approval never
```

---

## 💥 Destroying (careful 😅)

### Destroy all stacks

```bash
cdk destroy
```

### Destroy a specific stack

```bash
cdk destroy MyStack
```

---

## 📋 Stack Management

### List stacks in the app

```bash
cdk list
```

### Show stack metadata

```bash
cdk ls
```

---

## 🧪 Debugging & Troubleshooting

### Verbose output

```bash
cdk deploy --verbose
```

### Validate app

```bash
cdk doctor
```

---

## 🌍 Context & Environment

### View context values

```bash
cdk context
```

### Clear cached context

```bash
cdk context --clear
```

---

## 🧹 Cleanup & Reset

### Remove CDK toolkit stack

```bash
aws cloudformation delete-stack --stack-name MyStack
```

(Only if you *really* need to re-bootstrap.)

---

## 🔥 Most-used workflow (real life)

```bash
cdk diff
cdk deploy
```

That combo saves you from breaking prod 👀

---



