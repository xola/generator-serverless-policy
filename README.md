# Serverless Policy Generator

This is a yeoman generator for creating the AWS Policy document that 
allows a user to deploy a Serverless service.

Simply run it and provide it with the name of the service and, optionally,
the name of the stage and region for deployment (in case you want to limit the user
in question).

A `${project}-${stage}-${region}-policy.json` file will be created (using `_star_` instead of `*`
in the filename). The contents of this can then be used to create a policy in your IAM dashboard.

## Usage

This project requires [Yeoman](https://yeoman.io). Install globally with:

```
npm install -g yo
```

_NB as of 2020-03-05 this requires node >= v10_

Then install the generator:

```
npm install -y generator-serverless-policy
```

Now run in the directory in which you wish to output the policy JSON file:

```
yo serverless-policy
```

The generator will ask questions about region, stage, DynamoDB and S3 before outputting a policy. If this is the first time you have used Yeoman then Yeoman will prompt you about sharing analytics with them; _the answer to this does not affect the generation of the policy_.

## Acknowledgements

The basic Policy Document is taken from https://github.com/serverless/serverless/issues/1439#issuecomment-268434517
