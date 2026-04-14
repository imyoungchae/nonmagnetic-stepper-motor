---
layout: project_page
permalink: /

title: "Automated measurement of magnetic field uniformity in Helmholtz coils<br>using a nonmagnetic stepper motor"
authors:
  - Young-Chae Son, Sung-Jung Joo, Po-Gyu Park, Changjin Yun, Soo-Chul Lim* and Hyung-Kew Lee*
affiliations:
  - Dongguk University, KRISS, and KOREA University
---

<style>
h1.title {
  font-size: 2rem !important;
  line-height: 1.3;
}
</style>
<div class="is-size-6 has-text-centered" style="margin-top: -5rem; margin-bottom: 0.5rem; color: #555;">
  * Corresponding Authors
</div>
<div class="has-text-centered" style="margin-top: 0.8rem; margin-bottom: 1rem;">
  <p class="is-size-5" style="font-weight: 600;">
    Manuscript submitted to Measurement
  </p>
</div>
<div class="has-text-centered" style="margin-bottom: 2rem;">
  <a href="#" target="_blank" rel="noopener noreferrer"
     style="display: inline-block; margin: 0 0.4rem 0.6rem 0.4rem; padding: 0.75rem 1.6rem; background-color: #363636; color: white; border-radius: 999px; text-decoration: none; font-weight: 600; font-size: 1rem; box-shadow: 0 2px 6px rgba(0,0,0,0.12);">
    Paper
  </a>
</div>

<section class="hero teaser">
  <div class="container is-max-desktop">
    <div class="hero-body" style="padding-top: 0; padding-bottom: 2rem;">
      <h2 class="subtitle has-text-centered mt-3 is-size-6" style="color: #AE3A5D;">
        <strong>Interference-Free 3D Scanning System for Precision Magnetic Field Calibration</strong>
      </h2>
    </div>
  </div>
</section>

<div class="columns is-centered has-text-centered" style="margin-bottom: 2rem;">
  <div class="column is-four-fifths">
    <h2 class="title is-3">Abstract</h2>
    <div class="content has-text-justified">
      This study presents an automated scanning system for the measurement of magnetic field uniformity in a Helmholtz coil using a nonmagnetic pneumatic stepper motor. To avoid magnetic interference commonly introduced by electric motors, a custom-designed pneumatic stepper motor fabricated with nonmagnetic materials was employed to implement a three-dimensional scanning stage that moves the Hall sensor within the measurement volume of the Helmholtz coil. The stage automatically scanned a 4.8 × 4.8 × 4.8 cm³ volume by moving the Hall sensor in 1.2 cm increments along each axis. A total of 125 measurements were performed to complete a scan. The measured magnetic field uniformity of the tested Helmholtz coil was within ±0.43%, which is equivalent to the manually scanned result within the uncertainty of the magnetic field measurement. The automatic stage reduced the total scanning time from 90 minutes to 50 minutes as well as the human intervention time to 10 minutes, representing a more than 80% reduction without compromising measurement integrity. The uncertainty of the magnetic field measurement also improved by increasing the number of readings from the Hall sensor without a significant increase in measurement time.
    </div>
  </div>
</div>

<hr>

## Framework & System Design

<div class="content has-text-justified" style="margin-top: 10px;">
  <p>
    The automated scanning system was designed to completely eliminate magnetic disturbances, which are a critical limitation of conventional electric actuators in low-field magnetic measurements. The core of this system is a custom-designed pneumatic stepper motor driven entirely by compressed air.
  </p>
  <ul>
    <li><strong>100% Nonmagnetic Construction:</strong> The motor is fabricated using 3D-printed ABS and PLA components, plastic bearings, and commercially available syringes that act as pressure chambers.</li>
    <li><strong>Operating Principle:</strong> The motor utilizes four pneumatic pistons. By applying sequential air pressure to these pistons, it executes a "Lock-Push-Release" mechanism to achieve precise, bi-directional stepwise rotation of the geared axle.</li>
    <li><strong>Remote Control:</strong> The system is controlled by pneumatic regulators located far from the magnetically shielded room to ensure absolutely zero electrical interference during the calibration process.</li>
  </ul>
</div>

<br>

## Experiments & Measurement Protocol

<div class="container is-max-desktop">
  <div class="columns is-vcentered">
    <div class="column is-full">
      <div class="content has-text-justified">
        <p>
          The proposed system was experimentally validated at the Korea Research Institute of Standards and Science (KRISS). The automated translation stage was attached to the Helmholtz coil calibration setup to map the working volume.
        </p>
        <p>
          The scanning consisted of calculating the Relative Deviation of the magnetic flux density (RDB) across a 3D grid. The sensor automatically navigated 125 distinct positions, evaluating the spatial variation of the generated magnetic field from the center point. Because the system is automated, it allowed for higher-density data collection (20 sensor readings per point instead of 5) without delaying the overall process.
        </p>
      </div>
    </div>
  </div>
</div>

<hr>

<h2 class="title is-3 has-text-centered mt-6 mb-5">Key Achievements</h2>

<div class="box" style="background-color: #f5f5f5; border: 1px solid #e8e8e8; margin-bottom: 2rem;">
  <div class="columns is-centered">
    <div class="column">
      <div class="content">
        <h3 class="title is-5 has-text-centered">Time Efficiency & Automation</h3>
        <p class="has-text-centered">
          <strong>Total Time:</strong> Reduced from 90 minutes to 50 minutes.<br>
          <strong>Human Intervention:</strong> Drastically reduced from 90 minutes to just <strong>10 minutes</strong> (an 80%+ reduction), freeing operators from tedious manual knob-turning.
        </p>
      </div>
    </div>
    <div class="column">
      <div class="content">
        <h3 class="title is-5 has-text-centered">Measurement Reliability</h3>
        <p class="has-text-centered">
          <strong>Uniformity Result:</strong> Measured at ±0.43%, matching the manual scanning baseline perfectly.<br>
          <strong>Uncertainty Improvement:</strong> Decreased from ±0.11% to <strong>±0.06%</strong> due to the automated system's ability to seamlessly capture more readings per position.
        </p>
      </div>
    </div>
  </div>
</div>

<br>

<hr>

