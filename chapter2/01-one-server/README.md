# How to use

- Configure your AWS access keys as environment variables:

    ```
    export AWS_ACCESS_KEY_ID=(your access key id)
    export AWS_SECRET_ACCESS_KEY=(your secret access key)
    ```

- Deploy the code:
    ```
    terraform init
    terraform apply
    ```

- Clean up when you're done:
    ```
    terraform destroy
    ```