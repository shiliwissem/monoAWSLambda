# monoAWSLambda
Mono Built for AWS Lambda Container, you can use it to compile and run C# code on any lambda runtime
You can upload the ZIP file as a Lambda Layer and use it as binary from your Lambda function.

Example On Lambda  Nodejs Runtime
const childProcess=require('child_process');
const mono='/opt/monoLayer/bin/mono'; //opt is the default path for an attached layer
const csc='/opt/monoLayer/bin/csc';
//get the current version of mono
let result = childProcess.spawnSync(mono, ['--version'], {
        shell: true
});

console.log(result.stdout.toString());
