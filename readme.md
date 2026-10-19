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
flowchart LR
    subgraph SRC["① Source of truth"]
        direction TB
        MOD["Module library<br/><i>versioned, semver</i>"]
        STACK["Stacks<br/><i>one per environment</i>"]
        POL["Policy as code<br/><i>guardrails</i>"]
        MOD --> STACK
        POL --> STACK
    end

    subgraph CI["② Delivery pipeline"]
        direction TB
        VAL["validate · tflint · tfsec"]
        PLAN["plan"]
        GATE{"policy<br/>gate"}
        APPLY["apply"]
        VAL --> PLAN --> GATE
        GATE -->|pass| APPLY
        GATE -->|fail| STOP["blocked<br/><i>before it reaches prod</i>"]
    end

    subgraph CLOUDS["③ Landing zones"]
        direction TB
        GCP["Google Cloud<br/><i>hub-and-spoke · GKE</i>"]
        AZ["Microsoft Azure<br/><i>hub-and-spoke · AKS</i>"]
        IBM["IBM Cloud<br/><i>hub-and-spoke · IKS</i>"]
    end

    subgraph CONS["④ Consumers"]
        direction TB
        APP["Microservices"]
        DATA["Governed data products<br/><i>BigQuery Analytics Hub</i>"]
        OBS["Observability<br/>&amp; capacity planning"]
    end

    STACK --> VAL
    APPLY --> GCP
    APPLY --> AZ
    APPLY --> IBM
    GCP --> APP
    AZ --> APP
    IBM --> APP
    GCP --> DATA
    APP --> OBS
    DATA --> OBS
    OBS -.->|feeds sizing<br/>back into modules| MOD

    classDef src fill:#EEF2FF,stroke:#4F46E5,stroke-width:1px,color:#1E1B4B
    classDef ci fill:#ECFDF5,stroke:#059669,stroke-width:1px,color:#064E3B
    classDef cloud fill:#EFF6FF,stroke:#2563EB,stroke-width:1px,color:#0C2B5E
    classDef cons fill:#FFF7ED,stroke:#EA580C,stroke-width:1px,color:#431407
    classDef blocked fill:#FEF2F2,stroke:#DC2626,stroke-width:1px,color:#450A0A

    class MOD,STACK,POL src
    class VAL,PLAN,GATE,APPLY ci
    class GCP,AZ,IBM cloud
    class APP,DATA,OBS cons
    class STOP blocked
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
