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

- When the apply command completes, it will output the public IP address of the server. To test that IP:
    ```
    curl http://(server_public_ip):8080/
    ```

- Clean up when you're done:
    ```
    terraform destroy
    ```

- 備考
    - ここではデフォルトVPCにすべてのリソースをデプロイしている．デフォルトVPCのサブネットはすべてパブリックサブネットであり，インターネットからアクセス可能なIPアドレスが割り当てられるので，EC2インスタンスからアクセスできる．
    - 本番環境では，サーバやデータストアをプライベートサブネットに配置し，少数のリバースプロキシやロードバランサーのみをパブリックサブネットに配置する．