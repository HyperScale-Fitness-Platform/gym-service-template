# Repository Architecture & Template Convention

To maintain consistency across our microservices architecture and ensure seamless context-switching for any team member, **every single microservice repository must strictly adhere to the standardized skeleton structural template outlined below.** When initializing a new microservice, use `gym-<name>-service` as the naming convention and implement this exact directory layout.

---

## 📂 Repository Structural Skeleton

```text
gym-<name>-service/
├── src/                    # Core application source code
├── tests/                  # Unit, integration, and functional tests
├── Dockerfile              # Multi-stage build configuration for local and production images
├── k8s/                    # Local and environment-specific Kubernetes manifests
│   ├── deployment.yaml     # Pod configurations, replica limits, and container specs
│   ├── service.yaml        # Service definition mapping internal container ports
│   └── configmap.yaml      # Non-sensitive runtime environment variables for THIS service
├── .github/workflows/      # Automated CI/CD execution pipeline files
│   └── ci.yml              # CI pipeline script handling formatting, linting, testing, and container image builds
├── README.md               # Local service setup documentation, route details, and prerequisites
└── package.json            # Node.js project manifest, dependency configuration, and lifecycle scripts
