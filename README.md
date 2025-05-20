# Microsoft Fabric Deployment Pipeline Demo

This repository documents the step-by-step implementation of a deployment pipeline in **Microsoft Fabric**. The pipeline automates content movement across three environments: **Development**, **Test**, and **Production**.

## 📌 Overview

In this project, we used Microsoft Fabric’s built-in deployment pipelines to simulate a real-world CI/CD workflow. The main content item is a **Lakehouse**, built with sample data (NYCTaxi dataset).

---

## ✅ Steps Followed

### 1. Create Workspaces
- Created three Fabric workspaces: `Development`, `Test`, and `Production`.
- Enabled Fabric Trial on all workspaces.

### 2. Create a Deployment Pipeline
- Created a new pipeline via the Deployment Pipelines tab.
- Gave it a unique name and confirmed creation.

### 3. Assign Workspaces to Pipeline Stages
- Assigned each workspace to its corresponding stage:
  - Development → Development
  - Test → Test
  - Production → Production

### 4. Create Content in Development
- Created a new **Lakehouse** named `LabLakehouseS` in the Development workspace.
- Used the "Start with sample data" option and loaded the **NYCTaxi** dataset.

### 5. View Content in Pipeline
- Verified that the `LabLakehouseS` appeared under the Development stage in the pipeline canvas.

### 6. Deploy Content Across Stages
- First attempt from Development stage had UI issues (deploy button disabled).
- Instead, deployed from **Test** to **Production**, which worked successfully.
- Verified the green checkmarks indicating successful deployment in all stages.

---

## 🖼️ Screenshots

All screenshots documenting the process are located in the `/screenshots` directory. Each image corresponds to a step in the process and can be used for reference.

---

## 💬 Notes

- The UI bug preventing deployment from the Development stage is a known issue in Fabric trial environments.
- Workaround: deploy from Test to Production once the content exists in both.

---

## 🔗 Useful Links

- [Microsoft Fabric Deployment Pipelines Documentation](https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines-overview)
- [Lab Guide Used](https://microsoftlearning.github.io/mslearn-fabric/Instructions/Labs/21-implement-cicd.html)
