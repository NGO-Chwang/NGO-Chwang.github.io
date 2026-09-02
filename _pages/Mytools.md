---
layout: page
title: Tools & Projects
permalink: /tools/
description: "A collection of small tools, utilities, experimental applications, and personal software projects."
nav: true
nav_order: 6
---

## Tools & Projects

This page presents a collection of small tools, utilities, experimental applications, and personal software projects that I have developed for research, system monitoring, productivity, gaming, and other practical purposes.

Some projects are available as open-source software on GitHub.

---
## Lab Meeting Workflow Automation

To improve the consistency and efficiency of our weekly laboratory meetings, I reorganized the meeting workflow and developed several supporting tools for meeting preparation and management.

Because the meeting chair is rotated among students, meeting preparation was sometimes inconsistent, and meetings did not always start on time. To address this issue, I first reviewed and standardized the overall workflow, including chair assignment, topic and presenter planning, preparation of shared meeting folders, meeting-day setup, and post-meeting follow-up.

Based on this workflow, I developed and maintained several tools to reduce repetitive work and make meeting preparation easier for both the chair and the meeting coordinator.

### Automated Chair Reminder

I developed an automated email reminder tool that sends a notification to the chair scheduled for the following week.

The chair rotation is determined at the beginning of each semester, while suggested discussion topics are prepared based on previous meeting experience. The reminder is automatically sent every Wednesday at 10:00 AM.

This helps prevent cases in which the assigned chair is unaware of the upcoming responsibility and also reduces the amount of manual follow-up required from the meeting coordinator.

### Meeting Folder Management Tool

Meeting materials are stored on an Ubuntu-based shared server, where correct file and directory permissions are important.

In the past, users unfamiliar with Linux permissions could create meeting folders without the appropriate access settings, which sometimes prevented other members from uploading their presentation or report files.

To solve this problem, I developed a web-based folder management tool. The chair can select the meeting type, such as **CAS**, **LMM**, or the regular laboratory meeting, specify the meeting date, and create the required directory with a single operation.

The tool automatically creates the appropriate folder structure and applies the required file permissions, reducing setup errors and simplifying preparation for the chair.

### Progress Report / Presentation Merge Tool

Before each meeting, the chair needs to collect presentation files from laboratory members and combine them into a single file for presentation.

Because this process is repetitive and largely identical every week, I developed a tool that automatically reads presentation files (`.pptx`) from a specified directory and merges them according to a predefined mapping between users and filenames.

This reduced a task that previously required approximately **10–20 minutes** of manual work to **less than 5 minutes** in typical cases.

### Dedicated Meeting Computer Setup and Maintenance

I also maintain a dedicated computer for laboratory meetings.

Previously, the chair often needed to find an available laptop before the meeting and configure the necessary equipment and online meeting information each time.

The dedicated meeting computer is kept ready with commonly used meeting links, connection information, and device settings placed in easily accessible locations. This reduces meeting-day preparation and helps meetings start more smoothly.

### Impact

These workflow improvements and supporting tools have helped make the preparation process more consistent and reduced repetitive work for both meeting chairs and organizers.

The system provides a more structured workflow from chair assignment and meeting preparation through file management, presentation preparation, meeting-day setup, and follow-up, contributing to smoother and more reliable weekly laboratory meetings.
## GPU Server Monitor

**GPU Server Monitor** is a lightweight server monitoring application developed with **Streamlit** for monitoring the computing resources of our laboratory servers.

Our laboratory has multiple shared GPU servers that are used by students and researchers for deep learning experiments, medical image analysis, and other computational tasks. As the number of users increased, it became increasingly difficult to quickly understand which GPUs were available, which users were running jobs, and how long individual processes had been running.

To make GPU resource usage easier to understand, I developed this web-based monitoring tool.

### Main Features

The application collects and visualizes the current **CPU and GPU utilization** of laboratory servers. Resource usage is displayed using intuitive bar charts, allowing users to quickly identify available and heavily utilized computing resources.

In addition to overall resource utilization, the tool provides detailed information about individual processes running on each GPU, including:

- GPU utilization and memory usage;
- CPU utilization;
- running processes;
- the user associated with each process;
- process start time;
- detailed GPU usage for individual programs.
- Wheather GPU is health or not (temperture, programs size v.s. GPU)

One of the most useful features is the ability to identify **who is currently using each GPU and when the corresponding process was started**. This makes it much easier for laboratory members to understand the current GPU allocation and coordinate the use of shared computing resources.

<div class="row justify-content-center mt-3">
  <div class="col-md-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/gpu-monitor.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

<div class="caption">
  GPU Server Monitor showing CPU and GPU utilization and detailed information about running processes.
</div>

### Practical Use in the Laboratory

The system is currently used in our laboratory, which has approximately **40 students and researchers**. Most laboratory members who use the shared computing servers regularly access the monitoring system to check GPU availability before starting experiments.

By providing a centralized overview of GPU usage, the tool reduces the need to manually connect to individual servers or ask other users about resource availability.

The tool has received positive feedback from laboratory members, particularly for its simple interface and the ability to quickly identify available GPUs and understand ongoing computational workloads.
<div class="row justify-content-center mt-3">
  <div class="col-md-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/GPU-stat.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

<div class="caption">
  User statistics from August 19, 2026, to September 1, 2026 (the horizontal axis represents the last segment of the user's IPv4 address, and the vertical axis represents the number of visits; page refreshes are not counted)..
</div>
### Implementation

The monitoring interface is implemented using **Streamlit**, enabling the system to provide an accessible web-based dashboard without requiring users to install additional client software.

The application is designed primarily for use within a shared laboratory computing environment.

- **Framework:** Streamlit
- **Purpose:** Shared CPU/GPU resource monitoring
- **Users:** Approximately 40 laboratory members
- **Source code:** [GitHub](https://github.com/NGO-Chwang/GPU-monitor.git)

---

## Other Utilities

Additional small programs and experimental tools will be added here over time.
