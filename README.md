# microservices-udagram-cloud-dev-nanodegree

## Deployment instructions

### Setup Docker Environment
You'll need to install docker https://docs.docker.com/install/. Open a new terminal within the project directory and run:

1. Build the images: `docker-compose -f docker-compose-build.yaml build --parallel`
2. Push the images: `docker-compose -f docker-compose-build.yaml push`
3. Provide .env file with environment variables for docker compose. All variables are required
4. Run the container: `docker-compose up`

### Setup Kubernetes

1. You'll need to provide kubernetes infrastructure and deploy kubernetes. One way to do this is using kubeone. Follow instructions in order to do setup: https://github.com/kubermatic/kubeone/blob/master/docs/quickstart-aws.md
2. Initialize secrets (aws-secret, config-map, secret-map). Use base64 encoding for secret map and aws secret
3. run `kubectl apply -f k8s` from udacity-3-deployment folder. In order to deploy all resources including secrets
