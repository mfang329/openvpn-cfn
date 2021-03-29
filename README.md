Access aws Key ID & Secret Key from host.

create python virtual env
- need to script it

git clone {my repo}

run the cfn to create OpenVpn.
aws cloudformation deploy \
    --template-file openvpn-cfn/cfn-openvpn.yaml \
    --stack-name openvpn-personal \
    --profile $AWS_VPN_PROFILE \
    --parameter-overrides SSHKeyName=Heal-pubkey \
    --capabilities  CAPABILITY_IAM


This run will take about 10mins to create all the backend resources
- ec2
- s3 buckets
- vpc

- lambda