---
layout: default
title: Home
---

<!-- Custom header section -->
<div style="display: flex; align-items: center; gap: 20px; margin-top: 20px;">

  <img src="assets/headshot.jpg" alt="Profile photo"
       style="width:140px; height:180px; object-fit:cover; border-radius:8px;">

  <!-- Name and Links -->
  <div>
    <h1 style="margin: 0;">Bhaskar Pardeshi</h1>
    <p style="font-size: 1.1em; color: #555; margin-top: 4px;">
      Ph.D. Student, Computer Science<br>
      Georgia Institute of Technology<br>
      bpardeshi3 [@] gatech [.] edu
    </p>

    <!-- Social Icons -->
    <p style="margin-top: 10px;">
      <a href="https://github.com/bpardeshi3" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"
             alt="GitHub" width="26" height="26" style="vertical-align:middle;">
      </a>
      &nbsp;&nbsp;
      <a href="https://linkedin.com/in/bpardeshi" target="_blank">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg"
             alt="LinkedIn" width="26" height="26" style="vertical-align:middle;">
      </a>
      &nbsp;&nbsp;
      <a href="assets/resume.pdf" target="_blank">
        <img src="https://img.icons8.com/material-rounded/48/000000/resume.png"
             alt="Resume" width="26" height="26" style="vertical-align:middle;">
      </a>
    </p>
  </div>
</div>

<br>

# Bio
<p style="text-align: justify;">
Bhaskar is a second-year Ph.D. student in Computer Science at the Georgia Institute of Technology, advised by <a href="https://saeed.github.io/">Prof. Ahmed Saeed</a>. Before beginning the Ph.D. program, he worked for two years with VMware’s Datapath Networking team. He completed his undergraduate studies in Computer Engineering from the College of Engineering, Pune, in 2021.
</p>

# Research Interests
<p style="text-align: justify;">
<strong>Datacenter Networks and Systems</strong> - network congestion control, end-host network stacks, compute overload control, CPU scheduling (core-allocation and load-balancing).
</p>

# Publications
<ul style="list-style-type: disc; padding-left: 20px;">

  <li style="margin-bottom: 18px;">
    <strong>Svalinn: Overload Control in Large-Scale Servers with Multiple Resource Bottlenecks</strong><br>
    <span style="color: darkred;">Bhaskar Pardeshi</span>, Peidi Song, Ahmed Saeed<br>
    <a href="https://www.usenix.org/conference/osdi26">USENIX OSDI 2026</a>
    [[<a href="">Paper</a>]]
    [[<a href="">Code</a>]]
    [[<a href="javascript:void(0);" onclick="toggleAbstract('abstract-svalinn')">Abstract</a>]]

    <div id="abstract-svalinn"
         style="display: none; margin-top: 8px; padding: 10px; border-left: 3px solid #ccc; background: #f9f9f9; text-align: justify;">
    Modern overload controllers treat application binaries as monoliths and react to aggregate performance, a misconception we call the single-queue fallacy. Real applications have diverse, data-dependent execution paths that stress different resources. Reacting to overall performance forces the controller to focus on the most bottlenecked resource while leaving others underutilized.

    We present Svalinn, a modular overload controller designed to maximize utilization across multiple potential bottlenecks such as CPU, memory bandwidth, and contended locks. Svalinn separates throughput control and latency control. A credit-based admission controller regulates offered load to maximize a user-defined utility function. Per-bottleneck controllers then enforce latency targets using AQM-style mechanisms. For resources with explicit software queues this is straightforward, but managing memory bandwidth–intensive operations is more challenging because there is no explicit queue. To handle this case, we introduce "m_semaphore", which adaptively limits the number of concurrent memory bandwidth–intensive requests to achieve high memory-bandwidth utilization using the minimum necessary CPU cores. We integrate Svalinn into four applications and two runtimes and show that it improves throughput by up to 6.1x without compromising latency.
    </div>
  </li>

  <li style="margin-bottom: 18px;">
    <strong>CoreSync: A Protocol for Joint Core Scheduling and Overload Control of μs-Scale Tasks</strong><br>
    <span style="color: darkred;">Bhaskar Pardeshi</span>, Eric Stuhr, Ahmed Saeed<br>
    <a href="https://ieeeicnp2025.pages.dev/">IEEE ICNP 2025</a>
    [[<a href="assets/coresync-icnp25.pdf">Paper</a>]]
    [[<a href="https://github.com/GT-ANSR-Lab/CoreSync">Code</a>]]
    [[<a href="javascript:void(0);" onclick="toggleAbstract('abstract-coresync')">Abstract</a>]]

    <div id="abstract-coresync"
         style="display: none; margin-top: 8px; padding: 10px; border-left: 3px solid #ccc; background: #f9f9f9; text-align: justify;">
      Modern datacenter operators require high resource utilization and low application latency, multiplexing the resources of individual servers between multiple applications, while minimizing latency faced by their requests, even at high loads. To meet these objectives, servers employ multiple resource management algorithms, including fast core schedulers and overload controllers. Individual algorithms and their amalgamation are required to meet these tight performance requirements. In this paper, we demonstrate that state-of-the-art core schedulers and overload controllers produce poor performance when deployed simultaneously. Fundamentally, the design assumptions of each controller are violated by the other controller. An overload controller assumes that all resources are dedicated to an application, while a core scheduler assumes that all incoming load will be admitted. To overcome this fundamental limitation, we present CoreSync, a server-driven credit-based protocol for joint core scheduling and overload control. CoreSync relies on the basic idea that the admitted load should be proportional to the allocated resources. However, strict proportionality can lead to low utilization when admitted load does not materialize at the server (e.g., when demand drops). Thus, CoreSync uses partial proportionality to balance latency, throughput, and utilization. Our evaluation across synthetic and real-world workloads shows that CoreSync outperforms state-of-the-art schedulers and overload controllers. In particular, in overload scenarios, CoreSync improves throughput by up to 6%. At low loads, CoreSync reduces the 99th percentile latency by up to 1.7x and improves CPU utilization by up to 1.4x.
    </div>
  </li>

</ul>

<script>
  function toggleAbstract(id) {
    const elem = document.getElementById(id);
    if (elem.style.display === "none" || elem.style.display === "") {
      elem.style.display = "block";
    } else {
      elem.style.display = "none";
    }
  }
</script>

# Industry Experience
- **Nutanix, Inc.**<br>
  <span style="color: gray;">*May 2025 - Aug 2025*</span><br>
  Interned with the metadata storage team.
- **Nvidia**<br>
  <span style="color: gray;">*May 2024 - Aug 2024*</span><br>
  Interned with the notebook GPU's user-space power controller team.
- **VMware, Inc.**<br>
  <span style="color: gray;">*Jan 2021 - Jul 2023*</span><br>
  Worked at core ESX networking datapath team.

# Teaching Experience
- **Graduate Teaching Assistant (GTA), CS 8803 - Datacenter Networks & Systems**<br>
  <span style="color: gray;">*Jan 2026 - May 2026*</span><br>
  Georgia Institute of Technology
- **Graduate Teaching Assistant (GTA), CS 3251 - Computer Networking I**<br>
  <span style="color: gray;">*Aug 2023 - Dec 2023*</span><br>
  Georgia Institute of Technology
