
<h2 style="text-transform: capitalize;">Test Settings</h2>
<div align="left" style="position: relative;float:left;width:55%;">
    <ul style="line-height:150%">
      <li>Data size (n) </li>
        <ul style="list-style:none;">
          <li>(1.x) 2<sup>27</sup> (2.x) 201,326,592  (3.x) 2<sup>28</li>
        </ul>
        <li>Configurations</li>
    </ul>
<div class="fragment fade-in" data-fragment-index="2">
  <table>
    <tr style="border-bottom: 1px solid black;">
      <th>Setting</th>
      <th style="border-left: 1px solid black;">Taps (m)</th>
      <th style="border-left: 1px solid black;">Channels (k)</th>
    </tr>
    <tr style="border-bottom: 1px solid black;">
      <td>x.1</td>
      <td style="border-left: 1px solid black;">32</td>
      <td style="border-left: 1px solid black;">16</td>
    </tr>
    <tr>
      <td>x.2</td>
      <td style="border-left: 1px solid black;">16</td>
      <td style="border-left: 1px solid black;">64</td>
    </tr>
    <tr>
      <td>x.3</td>
      <td style="border-left: 1px solid black;">8</td>
      <td style="border-left: 1px solid black;">2048</td>
    </tr>
    <tr>
      <td>x.4</td>
      <td style="border-left: 1px solid black;">4</td>
      <td style="border-left: 1px solid black;">32768</td>
    </tr>
  </table>
</div>
</div>
<div class="fragment fade-in" data-fragment-index="2">
  <div align="left" style="position: relative;float:left;padding-top:10%;">
    <ul style="line-height:150%">
    <li >Taps: Number of multiplications for the filter \begin{aligned}
    \mathcal{O}(m\times n)
    \end{aligned} </li>
    <li >Channels: Batch size of the DFT \begin{aligned}
    \mathcal{O}(\log_{2}(k)\times n)
    \end{aligned} </li>
    </ul>
  </div>
</div>


---

<h2> Results GPU CPU</h2>
<ul>
  <li>High-level speedup <span class="highlight" style="color:green;">~ 17-96</span></li>
  <li>Low-level speedup <span class="highlight" style="color:green;">~ 5-37</span></li>
</ul>
<div align="left" style="width:100%;float:left;">
  <img alt="wwu-logo" width="80%"  data-src="images/MA_figures/GPUCPU.svg">
</div>


---

<h2> Results GPU CPU</h2>
<ul>
  <li>High-level speedup <span class="highlight" style="color:green;">~ 17-96</span></li>
  <li>Low-level speedup <span class="highlight" style="color:green;">~ 5-37</span></li>
</ul>
<div align="left" style="width:100%;float:left;">
  <img alt="wwu-logo" width="80%"  data-src="images/MA_figures/GPUCPU_stroke.svg">
</div>

---

## GPU Complete Runtime
<div align="left" style="width:80%;float:left;">
  <img alt="wwu-logo" width="100%"  data-src="images/MA_figures/GPGPU_total.svg">
</div>

---

## FIR-Filter
<div align="left" style="width:65%;float:left;">
  <img alt="wwu-logo" width="100%"  data-src="images/MA_figures/GPGPU_FIR.svg">
</div>

---

## FIR-Filter
<div align="left" style="width:65%;float:left;">
  <img alt="wwu-logo" width="100%"  data-src="images/MA_figures/GPGPU_FIR_stroke.svg">
</div>
<div align="left" style="width:35%;float:right;text-align:left;position: relative;">
  <table style="width:100%;">
    <tr style="border-bottom: 1px solid black;">
      <th>Setting</th>
      <th style="border-left: 1px solid black;">Approach</th>
      <th style="border-left: 1px solid black;">Speedup</th>
    </tr>
    <tr style="border: solid thick red;">
      <td>x.1</td>
      <td style="border-left: 1px solid black;">High-Level</td>
      <td style="border-left: 1px solid black;"><span class="highlight" style="color:green;">~1,6</span></td>
    </tr>
    <tr style="border-bottom: 1px solid black;">
      <td>x.2</td>
      <td style="border-left: 1px solid black;">Low-Level</td>
      <td style="border-left: 1px solid black;"><span class="highlight" style="color:green;">~2-2.1</span></td>
    </tr>
    <tr style="border-bottom: 1px solid black;">
      <td>x.3</td>
      <td style="border-left: 1px solid black;">Low-Level</td>
      <td style="border-left: 1px solid black;"><span class="highlight" style="color:green;">~2.7-2.8</span></td>
    </tr>
    <tr>
      <td>x.4</td>
      <td style="border-left: 1px solid black;">Low-Level</td>
      <td style="border-left: 1px solid black;"><span class="highlight" style="color:green;">~2.3</span></td>
    </tr>
  </table>
  <br>
  <h5 > Speedup constant over data sizes</h5>
</div>

---

## Discrete Fourier Transform
<div align="left" style="width:70%;float:left;">
<img alt="wwu-logo" width="100%"  data-src="images/MA_figures/GPGPU_DFT.svg">
</div>

---

## Discrete Fourier Transform
<div align="left" style="width:70%;float:left;">
<img alt="wwu-logo" width="100%"  data-src="images/MA_figures/GPGPU_DFT_stroke.svg">
</div>
<div  align="left" style="width:30%;float:right;text-align:left;position: relative;">
<div style="position: absolute;top: 50%;height: 30%;margin: 35% 0 0 0%;line-height=150%;">
  <ul style="line-height=150%">
    <li style="margin-bottom:20px;">For small sizes high-level</li>
    <li style="margin-bottom:20px;">Cufft library especially good for big data sizes</li>
  </ul>
</div>
</div>

---

## CuFFT Library Discrete Fourier Transform
<div align="left" style="width:100%;float:left;">
<img alt="wwu-logo" width="80%"  data-src="images/MA_figures/LL-DFT.svg">
</div>

---

<h2 align="center"> Max Planck Institut </h2>
<h2 align="center"> <font style="color:green;">125 ms</font></h2>
  <table style="align:left">
    <tr style="border-bottom: 1px solid black;">
      <th>Setting</th>
      <th style="border-left: 1px solid black;">Low-level with- <br>out cuFFT Plan</th>
      <th style="border-left: 1px solid black;">Low-level with <br>cuFFT Plan</th>
      <th style="border-left: 1px solid black;">High-level</th>
    </tr>
    <tr style="border-bottom: 1px solid black;">
      <td>3.1</td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">248.2389</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">457.7665</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">384.0984</font></td>
    </tr>
    <tr>
      <td>3.2</td>
      <td style="border-left: 1px solid black;"><font style="color:green;">61.1968</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">269.3751</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">449.5627</font></td>
    </tr>
    <tr>
      <td>3.3</td>
      <td style="border-left: 1px solid black;"><font style="color:green;">43.121</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">253.5033</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">727.7136</font></td>
    </tr>
    <tr>
      <td>3.4</td>
      <td style="border-left: 1px solid black;"><font style="color:green;">65.0726</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">274.6447</font></td>
      <td style="border-left: 1px solid black;"><font style="color:#a20101;">974.0683</font></td>
    </tr>
  </table>

---

## Memory Operations
<div align="left" style="width:70%;float:left;">
  <img alt="wwu-logo" width="100%"  data-src="images/MA_figures/GPGPU_Memory.svg">
</div>
<div  align="left" style="width:30%;float:right;text-align:left;position: relative;">
  <div style="position: absolute;top: 50%;height: 30%;margin: 15% 0 0 0%;">
    <h5>Reasons</h5>
    <ul>
      <li>Uneccessary memory transfers<span class="highlight" style="color:#852339;"></span></li>
      <li>Duplicates of all datastructures on the CPU<span class="highlight" style="color:#852339;"></span</li>
    </ul>
  </div>
</div>
