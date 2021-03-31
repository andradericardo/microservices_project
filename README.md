# Udacity Microservices project #

Deployment
----------
To deploy, create a `set_env.sh` file like below and run `source deploy.sh`

    # insert the secrets below and save this as set_env.sh
    export POSTGRES_USERNAME=<username>
    export POSTGRES_PASSWORD=<password>
    export POSTGRES_HOST=<host>
    export POSTGRES_DB=<database_name>
    export AWS_BUCKET=<S3_bucket>
    export AWS_REGION=<S3_region>
    export AWS_PROFILE=<AWS_profile>
    export JWT_SECRET=<random_string>
    export URL=http://localhost:8100


Commands for testing
--------------------

LOG INTO API-USER:

`kubectl exec --stdin --tty api-feed-557759fd9c-llfxb -- /bin/bash`


TEST API-USER:

    curl -X POST http://localhost:8080/api/v0/users/auth -H 'content-type: application/json' -d '{
    "email":"dummy@dummy.com",
    "password":"12345"
    }'


TEST API-FEED:

`curl -X GET http://api-feed:8080/api/v0/feed/3`
<<<<<<< HEAD


Check pods

kubectl describe pod podID
kubectl logs podID


To Create Secrets

http://blog.shippable.com/kubernetes-tutorial-using-secretes-in-your-kubernetes-application
=======
>>>>>>> 9f40d46c88fb1301881e774fa577f9784b1baeb3
