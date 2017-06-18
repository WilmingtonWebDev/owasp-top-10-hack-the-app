# Hack The Web

## Deploying the Juice shop App

### Locally using Docker

```
docker run -d -p 3000:3000 bkimminich/juice-shop
```

Then navigate to http://localhost:3000

Or:

```
sudo docker run -d -p 80:3000 bkimminich/juice-shop
```

Then navigate to http://localhost

### To AWS Instance (which also uses Docker)

Install ansible & boto

```
# Activate vituralenv
# then run
pip install -r requirements.txt
```

Run Playbook:
```
# export AWS credentials first
# then run
ansible-playbook \
    -e 'deploy_key_name=TomMGDeploy'
    owasp-top-10-hack-the-web.yml

```