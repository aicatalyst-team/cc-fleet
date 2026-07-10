# Blog Abstract: cc-fleet on OpenShift

**Thesis:** Deploying cc-fleet, a Go CLI for multi-model LLM provider orchestration, on OpenShift demonstrates how desktop-first developer tools can be containerized and validated on enterprise Kubernetes infrastructure.

**Target Audience:** Platform engineers and developers working with AI coding agents and multi-model LLM architectures.

**Blog Type:** Red Hat Developer Blog

**Key Points:**
1. A substantial Go CLI (391 files) compiles cleanly into a minimal UBI container using multi-stage builds
2. OpenShift binary builds handle the full pipeline from source to Quay registry without local container runtimes
3. CLI tools can be validated on Kubernetes using Job-based deployment patterns instead of long-running Deployments

**Products/Projects:** Red Hat OpenShift AI, Open Data Hub, UBI (Universal Base Image)

**CTA:** Explore how your own Go CLI tools can be containerized and validated on OpenShift using the AutoPoC pipeline.

**Section Outline:**
1. What is cc-fleet?
2. Why containerize a CLI tool?
3. Building with UBI multi-stage Dockerfiles
4. OpenShift binary builds: from source to registry
5. Job-based deployment for CLI validation
6. Test results and what we learned
7. Try it yourself
