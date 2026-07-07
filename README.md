# Repo template convention — every service repo should have the same skeleton so any team member can jump into any service:
gym-<name>-service/
├── src/
├── tests/
├── Dockerfile
├── k8s/                # deployment.yaml, service.yaml, configmap.yaml for THIS service
├── .github/workflows/  # ci.yml — lint, test, build image
├── README.md
└── package.json 
