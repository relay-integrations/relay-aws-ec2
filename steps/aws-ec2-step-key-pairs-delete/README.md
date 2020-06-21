# aws-ec2-step-key-pairs-delete

This [AWS EC2](https://aws.amazon.com/ec2/) step container deletes a set of key pairs
in an AWS account given a list of key pair names.

## Specification

| Setting | Child setting | Data type | Description | Default | Required |
|---------|---------------|-----------|-------------|---------|----------|
| `aws` || mapping | A mapping of AWS account configuration. | None | True |
|| `connection` | AWS Connection | Relay Connection for the AWS account. Use the Connection sidebar to configure the AWS Connection | None | True |
| `keyPairNames` | list | A list of key pair names to delete | 


## Example: List of Key Pair Names

```yaml
steps:
# ...
- name: delete-key-pairs
  image: relaysh/aws-ec2-step-key-pairs-delete
  spec:
   aws:
      connection: !Connection { type: aws, name: my-aws-account }
   keyPairNames:
   - key.pair.1
   - key.pair.2

```