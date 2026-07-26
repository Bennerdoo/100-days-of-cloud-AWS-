# 100 Days of Cloud (AWS)

Hands-on learning project covering Days 1–50: real-world AWS scenarios and core cloud concepts. Each day is a small, actionable task you can follow and reproduce in your own AWS account.

## Scope & Goals

- Cover practical, real-world tasks (Day 1 → Day 50).
- Teach foundational and advanced AWS concepts: IAM, EC2, VPC, S3, RDS, Networking, Load Balancing, Auto Scaling, Serverless, Containers (ECS/EKS), Infrastructure as Code (CloudFormation/Terraform), Monitoring (CloudWatch), Security, Cost optimization, backups, and more.
- Break large migrations and operations into safe, incremental steps.

## Repository Structure

- `Day 1 - Create Key pair.md`, `Day 2 - ...` — one Markdown file per day describing the task and commands.
- `images/` — supporting screenshots and diagrams referenced by day notes.

## Quick Start

Prerequisites:

- An AWS account with permissions to create the resources used in each day.
- `aws` CLI installed and configured (`aws configure`).

To view a day's instructions, open the corresponding Markdown file (for example, [Day 1 - Create Key pair.md](Day%201%20-%20Create%20Key%20pair.md)).

Example: Day 1 creates an EC2 key pair using the AWS CLI. The CLI command used in Day 1 saves the private key locally as `datacenter-kp.pem`.

Security note: do NOT commit private keys or other secrets into git. Add any generated `.pem` files to `.gitignore`.

## Usage

Run commands shown in each day's file from a secure workstation. Typical workflow:

1. Ensure `aws configure` is set with an account/profile that has the required permissions.
2. Run the example CLI commands (many examples assume the `default` profile).
3. Verify resources using `aws` CLI or the AWS Console.

## Contributing

- Add or edit daily notes as `Day <n> - <Title>.md`.
- Keep examples reproducible and include any cleanup steps.
- Open a pull request with a clear description and test steps.

## Notes

- This series stops at Day 50 and focuses on practical, repeatable tasks that mirror real operational needs in AWS.
- If you want variants (PowerShell commands, Terraform/CloudFormation templates, or additional verification steps), open an issue or submit a PR.
