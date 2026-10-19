<h1 align="center">Matheus Americano</h1>

<p align="center">
  <strong>Cloud Infrastructure Architect</strong><br>
  Multi-cloud platforms for regulated, high-stakes environments
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheusamericano">
    <img src="https://img.shields.io/badge/LinkedIn-matheusamericano-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <img src="https://img.shields.io/badge/Based_in-Belo_Horizonte,_BR-1A3157?style=flat-square" alt="Location">
  <img src="https://img.shields.io/badge/Open_to-international_consulting-3B82F6?style=flat-square" alt="Open to">
</p>

---

I build the Terraform standards and Kubernetes platforms that regulated,
high-criticality environments run on — the kind where every change is auditable
and downtime is not an option. I work across three clouds, lead cloud squads
technically, and teach the same material as a Microsoft Certified Trainer.

### Platforms & tooling

![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Microsoft Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![IBM Cloud](https://img.shields.io/badge/IBM_Cloud-052FAD?style=for-the-badge&logo=ibmcloud&logoColor=white)

![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=helm&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=for-the-badge&logo=googlebigquery&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?style=for-the-badge&logo=azuredevops&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

### How I think about platform work

```mermaid
flowchart TB
    subgraph GOV["Governance layer"]
        POL["Policies &<br/>guardrails"]
        ID["Identity &<br/>access"]
    end

    subgraph IAC["Infrastructure as Code"]
        MOD["Versioned<br/>module library"]
        PIPE["CI pipelines<br/>plan · policy · apply"]
    end

    subgraph PLAT["Platform layer"]
        NET["Network<br/>topology"]
        K8S["Kubernetes<br/>clusters"]
        DATA["Governed<br/>data products"]
    end

    subgraph RUN["Workloads"]
        APP["Microservices"]
        ANA["Analytics<br/>consumers"]
    end

    POL --> PIPE
    ID --> PIPE
    MOD --> PIPE
    PIPE --> NET
    PIPE --> K8S
    PIPE --> DATA
    NET --> APP
    K8S --> APP
    DATA --> ANA
```

Reusable modules are the unit of governance: if the baseline is correct in the
module, every environment inherits it — and the pipeline, not a checklist,
is what enforces it.

### Focus areas

| Area | What that means in practice |
|---|---|
| **Infrastructure as Code at scale** | Versioned module libraries, semantic releases, policy-as-code in the pipeline |
| **Multi-cloud landing zones** | Project/subscription hierarchy, network topology, identity federation, guardrails |
| **Kubernetes platform engineering** | Cluster baselines, RBAC, network policy, ingress and observability across GKE, AKS and IKS |
| **Resilience & capacity** | Sizing and hardening for critical, time-boxed traffic events at national scale |
| **Data platform architecture** | Hub-and-spoke designs that let business units share data products under central governance |
| **Enablement** | Turning architecture decisions into documentation and training that outlive the project |

### Certifications

[![GCP Professional Cloud Architect](https://img.shields.io/badge/Google_Cloud-Professional_Cloud_Architect-4285F4?style=flat-square&logo=googlecloud&logoColor=white)](https://www.credly.com/users/matheus-americano)
[![Azure Solutions Architect Expert](https://img.shields.io/badge/Microsoft-Azure_Solutions_Architect_Expert-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)](https://learn.microsoft.com/users/)
[![DevOps Engineer Expert](https://img.shields.io/badge/Microsoft-DevOps_Engineer_Expert-0078D4?style=flat-square&logo=azuredevops&logoColor=white)](https://learn.microsoft.com/users/)
[![MCT](https://img.shields.io/badge/Microsoft-Certified_Trainer-F25022?style=flat-square&logo=microsoft&logoColor=white)](https://www.microsoft.com/learning/mct-certification.aspx)

### Currently

- Technical lead for cloud squads in a highly regulated financial environment
- Publishing reference architectures and reusable Terraform modules here
- Studying for **HashiCorp Terraform Associate (004)** and **CKA**
- Teaching official Microsoft courses as an MCT

### Languages

Portuguese (native) · English (professional working) · Spanish (basic)

<p align="center">
  <sub>Everything published here is reference material written from scratch — no client code, configuration or data.</sub>
</p>
