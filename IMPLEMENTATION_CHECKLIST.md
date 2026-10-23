# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] POST /drift returns JSON with fields: psi, ks, wasserstein, overall_score
- [ ] Overall_score > 0.7 triggers an alert in the UI
- [ ] Response latency < 200 ms for 1 k records
- [ ] Dashboard auto‑refreshes every minute
- [ ] Charts correctly plot last 24 h of metrics
- [ ] User can configure alert thresholds
- [ ] Pipeline logs appear in MLflow UI
- [ ] New model version has tag 'auto‑retrained'
- [ ] Previous version remains queryable
- [ ] Alert payload includes model_id, metric, value, and suggested action
- [ ] Test webhook receives JSON within 5 seconds
- [ ] Set up FastAPI project, Dockerfile, PostgreSQL schema
- [ ] Implement /drift endpoint and Redis queue
- [ ] Create synthetic dataset and reference statistics
- [ ] Unit tests for drift calculations (pytest)
- [ ] Integration test: send 1k records, verify DB entry and alert
- [ ] Load test with locust: 5 k rps, ensure <200 ms latency
- [ ] Security test: OWASP ZAP scan of FastAPI endpoints
- [ ] Build multi‑stage Docker image
- [ ] Deploy PostgreSQL, Redis, and API on Docker‑Compose for local demo
- [ ] Push image to Docker Hub
- [ ] GitHub Actions CI builds image, runs tests, and pushes to a managed Kubernetes cluster (e.g., Render or Fly.io)

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
