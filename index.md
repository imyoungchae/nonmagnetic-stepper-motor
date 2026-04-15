---
layout: project_page
permalink: /

title: "Automated measurement of magnetic field uniformity in Helmholtz coils<br>using a nonmagnetic stepper motor"
authors:
  - Young-Chae Son¹, Sung-Jung Joo², Po-Gyu Park², Changjin Yun³, Soo-Chul Lim¹* and Hyung-Kew Lee²*
affiliations:
  - ¹ Dongguk University, ² KRISS, ³ KOREA University
---


<div class="is-size-6 has-text-centered" style="margin-top: -5rem; margin-bottom: 0.5rem; color: #555;">
  * Corresponding Authors
</div>
<div class="has-text-centered" style="margin-top: 0.8rem; margin-bottom: 1rem;">
  <p class="is-size-5" style="font-weight: 600;">
    Under Review
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
        <strong>Nonmagnetic 3D Scanning System for Magnetic Field Calibration</strong>
      </h2>
    </div>
  </div>
</section>

<div class="columns is-centered has-text-centered" style="margin-bottom: 2rem;">
  <div class="column is-four-fifths">
    <h2 class="title is-3">Abstract</h2>
    <div class="content has-text-justified">
      This study presents an automated scanning system for the measurement of magnetic field uniformity in a Helmholtz coil using a nonmagnetic pneumatic stepper motor. To avoid magnetic interference commonly introduced by electric motors, a custom-designed pneumatic stepper motor fabricated with nonmagnetic materials was employed to implement a three-dimensional scanning stage that moves the Hall sensor within the measurement volume of the Helmholtz coil. The stage automatically scanned a 4.8 × 4.8 × 4.8 cm³ volume by moving the Hall sensor in 1.2 cm increments along each axis. A total of 125 measurements were performed to complete a scan. The measured magnetic field uniformity of the tested Helmholtz coil was within ±0.43%, which is consistent with the manually scanned result within the uncertainty of the magnetic field measurement. The automatic stage reduced the total scanning time from 90 minutes to 50 minutes and the human intervention time from 90 minutes to 10 minutes. The uncertainty of the magnetic field measurement was also reduced by increasing the number of readings from the Hall sensor without a significant increase in measurement time.
    </div>
  </div>
</div>

<hr>

## Motivation

<div class="container is-max-desktop">
  <div class="content has-text-justified">
    <p>
      Helmholtz coils are commonly employed to generate uniform magnetic fields for the calibration of magnetic sensors and magnetometers. They are critical instruments for providing traceability for low magnetic field sensors and standards in the range from 0.1 mT to 20 mT. Calibrating a Helmholtz coil requires two tasks: (1) determining the <strong>coil constant</strong>, which relates the input current to the output magnetic field, and (2) evaluating the <strong>uniformity</strong> of the generated field within a specified working volume.
    </p>
    <p>
      At KRISS (Korea Research Institute of Standards and Science), the uniformity evaluation is performed by scanning the working volume with a Hall sensor attached to a three-axis translation stage. However, <strong>conventional electrical actuators cannot be used</strong> for this scanning because they generate magnetic fields — some stepper motors produce fields in the range of tens of microteslas to over 100 µT — that would corrupt the measurement. This forces the operator to manually turn the mechanical knobs of the translation stage throughout the entire scanning process, making the calibration time-consuming (~90 minutes) and susceptible to human errors.
    </p>
    <p>
      To address this limitation, we propose an automated scanning system using a <strong>custom-designed nonmagnetic pneumatic stepper motor</strong>. The motor operates solely on compressed air and is fabricated entirely from nonmagnetic materials, enabling precise sensor positioning without disturbing the magnetic field being measured.
    </p>
  </div>
</div>

<hr>

## Framework & System Design

<div class="content has-text-justified" style="margin-top: 10px;">
  <p>
    The automated scanning system was designed to eliminate magnetic disturbances caused by conventional electric actuators in low-field magnetic measurements. The core of this system is a custom-designed pneumatic stepper motor driven by compressed air.
  </p>
  <ul>
    <li><strong>Nonmagnetic Construction:</strong> The motor is fabricated using 3D-printed ABS and PLA components, plastic bearings (POM and Glass), and commercially available disposable syringes (3 mL) that serve as pressure chambers. All fasteners use nonmagnetic polymers (polyphenylene sulfide and polyamide MXD6).</li>
    <li><strong>Operating Principle:</strong> The motor utilizes four pneumatic pistons arranged perpendicular to the axis of rotation. By applying sequential air pressure to these pistons, it executes a "Lock-Push-Release" mechanism to achieve bi-directional stepwise rotation of the geared axle. The step angle is 10°, defined by the axial misalignment between two nine-tooth gears.</li>
    <li><strong>Performance:</strong> At 0.3 MPa input pressure, the motor generates 1.91 Nm of output torque — far exceeding the 6.6 mNm minimum required to move the translation stage. A full 360° rotation (nine 40° cycles) completes in 2.16 seconds, yielding approximately 27.3 RPM under short-tube conditions.</li>
    <li><strong>Remote Control:</strong> The system is controlled by pneumatic regulators (SMC ITV0031-2BL) located at least three meters away from the measurement setup to prevent electrical interference. A LabVIEW program running on an NI USB-6001 DAQ module generates the sequential pressure signals for motor operation.</li>
  </ul>
</div>

<!-- Fig. 3 and Fig. 4 side by side with unified caption -->
<div class="columns is-centered" style="margin-top: 1.5rem; margin-bottom: 0;">
  <div class="column is-four-fifths">
    <div class="columns is-vcentered is-mobile" style="margin-bottom: 0;">
      <div class="column is-half">
        <img src="static/image/fig3.png" alt="Motor structure" style="width: 100%; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      </div>
      <div class="column is-half">
        <img src="static/image/fig4.png" alt="Motor operation principle" style="width: 100%; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      </div>
    </div>
    <figcaption style="margin-top: 0.75rem; margin-bottom: 2rem; font-size: 0.92rem; color: #444; line-height: 1.6; text-align: center;">
      <strong>Fig. 3 &amp; 4.</strong> (Left) Exploded and assembled views of the pneumatic stepper motor, showing the housing, geared axle, pistons, pressure chambers, and plastic bearings. (Right) The stepping mechanism: two nine-tooth gears with a 10&deg; rotational offset enable bi-directional stepwise rotation through sequential piston actuation (steps 1-1 to 4-2).
    </figcaption>
  </div>
</div>

<div class="columns is-centered" style="margin-top: 1.5rem; margin-bottom: 2rem;">
  <div class="column is-four-fifths">
    <figure>
      <video src="static/image/pneumatic_motor.mp4" autoplay muted loop playsinline style="width: 100%; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);"></video>
      <figcaption style="margin-top: 0.75rem; font-size: 0.92rem; color: #444; line-height: 1.6;">
        <strong>Video.</strong> Demonstration of the nonmagnetic pneumatic stepper motor in operation.
      </figcaption>
    </figure>
  </div>
</div>

<div class="content has-text-justified">
  <p>
    The motor's stepping mechanism is based on two sets of nine-tooth gears with a 10° rotational offset. When pressure is applied to a piston, it engages with one gear to latch and lock the axle. A subsequent piston then pushes the second gear, and when the first piston releases, the axle rotates by one step angle. This <strong>Lock-Push-Release</strong> sequence is repeated to produce continuous rotation, and reversing the step order reverses the rotation direction. Eight steps complete a 40° rotation, and nine such cycles produce a full 360° revolution. The use of commercial syringe barrels and rubber bulbs as pressure chambers and seals eliminated the need to re-engineer sealing components, significantly simplifying the fabrication process.
  </p>
</div>

<br>

## Experiments & Measurement Protocol

<div class="container is-max-desktop">
  <div class="columns is-vcentered">
    <div class="column is-full">
      <div class="content has-text-justified">
        <p>
          The proposed system was experimentally validated at the Korea Research Institute of Standards and Science (KRISS). All measurements were conducted inside a magnetically silent environment where three orthogonally aligned cancellation coils (approximately 2 m in diameter) suppress external magnetic interference, including the geomagnetic field, to below ±1 nT. The automated translation stage was attached to the Helmholtz coil calibration setup to map the working volume.
        </p>
      </div>
    </div>
  </div>
</div>

<div class="columns is-centered" style="margin-top: 1.5rem; margin-bottom: 2rem;">
  <div class="column is-four-fifths">
    <figure>
      <img src="static/image/fig1.png" alt="Fig. 1" style="width: 100%; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      <figcaption style="margin-top: 0.75rem; font-size: 0.92rem; color: #444; line-height: 1.6;">
        <strong>Fig. 1.</strong> (a) Measurement system for the calibration of Helmholtz coils. The DUT Helmholtz coil is placed inside the cancellation coils with a diameter of 2 m to suppress external magnetic interference. Each coil is independently driven by a precision current source. (b) A Cs-⁴He magnetometer, used as a reference for coil constant measurement, and a Hall sensor attached to a three-dimensional manual translation stage installed inside the cancellation coils.
      </figcaption>
    </figure>
  </div>
</div>

<div class="container is-max-desktop">
  <div class="content has-text-justified">
    <p>
      The scanning protocol involved calculating the <strong>Relative Deviation of the magnetic flux density (RDB)</strong> across a 3D grid using Equation (1):
    </p>
    <p style="text-align: center; font-size: 1.1rem; margin: 1rem 0;">
      RDB = (B(x, y, z) − B<sub>center</sub>) / B<sub>center</sub> × 100 %
    </p>
    <p>
      The sensor automatically navigated 125 distinct positions (a 5 × 5 × 5 grid with 1.2 cm spacing) within the 4.8 × 4.8 × 4.8 cm³ working volume, measuring the spatial variation of the generated magnetic field relative to the center point. The magnetic flux density at the center was approximately 100 µT. A Hall sensor magnetometer (Lakeshore Cryotronics F71) with an RMS noise of 120 nT was used for field mapping. Because the system is automated, it enabled a higher number of sensor readings per point (20 instead of 5) without increasing the overall measurement time. The position accuracy was verified to be far less than 1 mm (the minimum scale of the stage rulers), and the accumulated position error after a full 125-point scan was also well below 1 mm.
    </p>
  </div>
</div>

<div class="columns is-centered" style="margin-top: 1.5rem; margin-bottom: 2rem;">
  <div class="column is-four-fifths">
    <figure>
      <img src="static/image/fig2.png" alt="Fig. 2" style="width: 60%; margin: 0 auto; display: block; border-radius: 6px; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
      <figcaption style="margin-top: 0.75rem; font-size: 0.92rem; color: #444; line-height: 1.6;">
        <strong>Fig. 2.</strong> (a) Three-dimensional grid of 125 measurement points for evaluation of magnetic field uniformity in the KRISS Helmholtz coil. (b) Three-dimensional plot of RDBs measured by manually scanning the 125 points in the grid.
      </figcaption>
    </figure>
  </div>
</div>

<hr>

<h2 class="title is-3 has-text-centered mt-6 mb-5">Results</h2>

<div class="container is-max-desktop">
  <div class="content has-text-justified">
    <p>
      The automated scanning results were compared with the manual scanning baseline. The key findings are summarized below:
    </p>
  </div>
</div>

<div class="container is-max-desktop" style="margin-bottom: 1.5rem;">
  <table class="table is-bordered is-striped is-hoverable is-fullwidth" style="font-size: 0.95rem;">
    <thead>
      <tr>
        <th style="text-align: center;">Metric</th>
        <th style="text-align: center;">Manual Scanning</th>
        <th style="text-align: center;">Automatic Scanning</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Field Uniformity</td>
        <td style="text-align: center;">±0.39%</td>
        <td style="text-align: center;">±0.43%</td>
      </tr>
      <tr>
        <td>Max RDB Position</td>
        <td style="text-align: center;">(-2.4, 2.4, 2.4) cm</td>
        <td style="text-align: center;">(-2.4, 2.4, 2.4) cm</td>
      </tr>
      <tr>
        <td>Readings per Point</td>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">20</td>
      </tr>
      <tr>
        <td>Measurement Uncertainty (k=2)</td>
        <td style="text-align: center;">±0.11%</td>
        <td style="text-align: center;">±0.06%</td>
      </tr>
      <tr>
        <td>RDB Uncertainty (k=2)</td>
        <td style="text-align: center;">±0.16%</td>
        <td style="text-align: center;">±0.09%</td>
      </tr>
      <tr>
        <td>Total Scanning Time</td>
        <td style="text-align: center;">~90 min</td>
        <td style="text-align: center;">~50 min</td>
      </tr>
      <tr>
        <td>Human Intervention Time</td>
        <td style="text-align: center;">~90 min</td>
        <td style="text-align: center;">~10 min</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="container is-max-desktop">
  <div class="content has-text-justified">
    <p>
      The measured magnetic field uniformity was within ±0.43% for the automatic scan, compared to ±0.39% for manual scanning. The difference of only 0.04% is well within the measurement uncertainty of ±0.16% (k=2), confirming that the pneumatic motor introduced <strong>no measurable magnetic interference</strong>. The maximum RDB was observed at the same corner position (-2.4 cm, 2.4 cm, 2.4 cm) in both methods, and the spatial patterns of the 3D field maps were nearly identical.
    </p>
    <p>
      The automated system also improved measurement quality: by averaging 20 Hall sensor readings per point (instead of 5 in manual mode), the type A uncertainty of the magnetic flux density measurement was reduced from ±110 nT (±0.11%) to ±60 nT (±0.06%). In terms of time efficiency, the total scanning time was reduced from 90 minutes to 50 minutes (~44% reduction), while the required human intervention time decreased dramatically from 90 minutes to just 10 minutes (>80% reduction). Three repeated full scanning cycles confirmed excellent repeatability, with all measurements agreeing within their respective uncertainties.
    </p>
  </div>
</div>

<hr>
