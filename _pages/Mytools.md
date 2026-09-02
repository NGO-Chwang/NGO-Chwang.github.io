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
## Lab Meeting Workflow Automation and Operational Support

To improve the consistency and efficiency of our weekly laboratory meetings, I reorganized the meeting workflow and developed several supporting tools and operational practices for meeting preparation and management.

Our laboratory holds weekly group meetings, and the role of meeting chair rotates among students. Because of this rotation, meeting preparation was sometimes inconsistent, and meetings did not always start smoothly or on time. To address this issue, I first reviewed and organized the overall workflow, including chair assignment, topic and presenter planning, preparation of shared meeting folders, meeting-day setup, attendance confirmation, and post-meeting follow-up.

Based on this workflow, I introduced several practical tools and management improvements to reduce repetitive work, simplify preparation, and support smoother operation of weekly meetings.

<div class="row justify-content-center mt-3">
  <div class="col-md-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/MeetingLeader.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>

<div class="caption">
  Workflow overview of weekly laboratory meeting operations and the supporting tools introduced to improve efficiency, consistency, and meeting management.
</div>

### Workflow Organization

I clarified and standardized the overall workflow of weekly laboratory meetings, including:

- chair assignment;
- planning of meeting topics and presenters;
- preparation of the shared meeting folder;
- meeting-day setup;
- attendance confirmation;
- meeting execution and follow-up.

This made the responsibilities of each step clearer and helped establish a more consistent meeting process.

### Automated Chair Reminder Tool

I developed an automated email reminder tool to support the weekly chair rotation.

The tool sends reminder emails to the student assigned to chair the upcoming meeting and also helps communicate suggested agenda items. This reduces the risk that the assigned chair is unaware of the responsibility and helps lower the burden on the meeting coordinator.

### Meeting Folder Management Tool

Meeting materials are stored on an Ubuntu-based shared server, where correct folder structure and file permissions are important.

To make this process easier and more reliable, I developed a web-based folder management tool that allows users to create meeting folders according to the meeting type, such as **CAS**, **LMM**, or the regular laboratory meeting. The tool automatically prepares the required folder structure and applies appropriate file permissions, reducing setup errors and simplifying preparation for the chair.

### Progress Report / Presentation Merge Tool

Before each meeting, the chair needs to collect presentation files from laboratory members and combine them into a single file for presentation.

Because this process is repetitive and largely the same every week, I developed a tool that automatically reads presentation files (`.pptx`) from a specified directory and merges them according to a predefined mapping between users and filenames.

This significantly reduces manual effort and helps the chair prepare the final presentation materials more efficiently.

### Meeting Attendance Check-in and Status Tracking Tool

I also developed a tool for attendance check-in at the beginning of laboratory meetings.

Attendance is confirmed manually for each participant, and the system records participation status such as **present, sick leave, class, business trip,** or **personal reasons**. These records are stored over time, making it possible to summarize and visualize each member’s attendance status for the current year.

This helps the professor and meeting organizers better understand students’ participation patterns and overall attendance conditions, while also making attendance management more systematic.

### Dedicated Meeting Computer Setup and Maintenance

In addition to software tools, I also maintain a dedicated computer environment for laboratory meetings.

Previously, the chair often needed to find an available laptop before the meeting and prepare the required setup each time. To make the process more reliable, I helped maintain a dedicated meeting computer and organized commonly needed information, such as meeting links, connection information, and device setup, so that meetings can begin more smoothly.

### Impact

These workflow improvements and supporting tools have helped make weekly laboratory meetings more structured, efficient, and reliable.

The improvements reduced repetitive manual work, simplified preparation for rotating student chairs, supported more consistent meeting operation, and provided better visibility into attendance and meeting readiness. Overall, they contributed to smoother weekly meetings and more systematic laboratory operations.
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
