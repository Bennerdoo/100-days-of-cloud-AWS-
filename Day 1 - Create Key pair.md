# Question

The Nautilus DevOps team is strategizing the migration of a portion of their infrastructure to the AWS cloud. Recognizing the scale of this undertaking, they have opted to approach the migration in incremental steps rather than as a single massive transition. To achieve this, they have segmented large tasks into smaller, more manageable units. This granular approach enables the team to execute the migration in gradual phases, ensuring smoother implementation and minimizing disruption to ongoing operations. By breaking down the migration into smaller tasks, the Nautilus DevOps team can systematically progress through each stage, allowing for better control, risk mitigation, and optimization of resources throughout the migration process.

## Task

For this task, create a key pair with the following requirements:

- Name of the `key pair` should be `<yourkeyname>-kp`.
- Key pair `type` must be `rsa`.

## Step-by-step Solution

Here is how you can create the AWS key pair using the AWS CLI:

### Command

Bash

```bash
aws ec2 create-key-pair \
	--key-name <yourkeyname>-kp \
	--key-type rsa \
	--query 'KeyMaterial' \
	--output text > yourkeyname-kp.pem
```

### Key Details & Post-Steps

- **`--key-name <yourkeyname>-kp`**: Sets the name of the key pair in AWS.
- **`--key-type rsa`**: Specifies the RSA key algorithm as required.
- **`--query 'KeyMaterial' --output text > <yourkeyname>-kp.pem`**: Saves the private key output directly into a local `.pem` file so you can use it for SSH access.

#### Set File Permissions
After generating the key, restrict its permissions so SSH allows you to use it:

Bash

```bash
chmod 400 <yourkeyname>-kp.pem
```

#### Verification
To verify that the key pair was successfully created in AWS, run:

Bash

```bash
aws ec2 describe-key-pairs --key-names <yourkeyname>-kp
```


