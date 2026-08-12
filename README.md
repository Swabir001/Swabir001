<!-- ════════════════════════════ HERO ════════════════════════════ -->

<div align="center">

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hero.png" width="100%" alt="Swabir M. Bwana"/>

<img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=600&size=22&pause=1100&color=E50914&center=true&vCenter=true&width=760&height=42&lines=react+and+node+that+ships+to+real+users;interrupt-driven+C+on+bare+metal;crawlers%2C+indexes+and+UDP+servers+in+plain+C;neural+nets+synthesized+into+FPGA+logic" alt="focus"/>

&nbsp;

[![site](https://img.shields.io/badge/SITE-swabir.com-E50914?style=for-the-badge&labelColor=0A0A0A)](https://swabir.com)
[![linkedin](https://img.shields.io/badge/LINKEDIN-swabir--mohamed-F5F5F5?style=for-the-badge&labelColor=0A0A0A)](https://www.linkedin.com/in/swabir-mohamed-927086271/)
[![email](https://img.shields.io/badge/EMAIL-dartmouth.edu-E50914?style=for-the-badge&labelColor=0A0A0A)](mailto:swabir.m.bwana.27@dartmouth.edu)

</div>

<!-- ════════════════════════════ 01 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-profile.png" width="100%" alt="01 Profile"/>

I write software and firmware, and I don't treat them as two separate careers. Some weeks that means a React and Node platform with real users hitting it in production. Other weeks it's an interrupt handler on a Cortex-M0 where the entire job is shaving microseconds. The engineers I learn the most from are comfortable on both sides of that line, so that's where I'm trying to stand.

|  |  |
|:--|:--|
| **PROGRAM** | Engineering Sciences modified with Computer Science · Thayer School of Engineering |
| **BASE** | Hanover, NH · originally from Mombasa, Kenya |
| **SHIPPING** | QlikShift, a production shift-scheduling SaaS running inside Dartmouth Library |
| **TEACHING** | TA · CS10 Object-Oriented Programming · previously ENGS 28 Embedded Systems |
| **OPEN TO** | <img src="https://img.shields.io/badge/NEW%20GRAD-2027-E50914?style=flat-square&labelColor=0A0A0A"/> software engineering · firmware · systems · hardware-software integration |

<!-- ════════════════════════════ 02 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-software.png" width="100%" alt="02 Software"/>

<a href="https://github.com/dartmouth-cs52-25S/project-swipe-plate"><img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-swipeplate.png" width="100%" alt="SwipePlate"/></a>

Campus food delivery across all four Dartmouth dining halls, where students order and other students deliver. I led a team of four from an empty repo to a deployed product in six weeks, and built both halves myself: two decoupled repos wired to the real campus dining API rather than mock JSON.

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#141417','primaryTextColor':'#f5f5f5','primaryBorderColor':'#E50914','lineColor':'#E50914','clusterBkg':'#0a0a0c','clusterBorder':'#E50914','fontFamily':'ui-monospace, monospace','fontSize':'13px'}}}%%
flowchart LR
    subgraph FE["FRONTEND · React 18 + TypeScript + Vite"]
        R["15+ route components<br/>browse · order · track · driver"]
        M["React Leaflet<br/>live delivery map"]
        H["custom hook<br/>live Dartmouth dining API"]
    end
    subgraph BE["BACKEND · Node + Express"]
        E["8 REST endpoints<br/>users · wallet · order lifecycle"]
        S["Firebase Admin SDK<br/>service-account auth"]
    end
    DB[("Firestore<br/>users · orders")]
    R --> M
    R --> H
    FE -->|"REST / JSON"| BE
    E --> S --> DB
```

<a href="https://github.com/Swabir001/tse-Swabir001"><img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-tse.png" width="100%" alt="Tiny Search Engine"/></a>

Three separate C programs that pipe into each other, with nothing external doing the hard parts.

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#141417','primaryTextColor':'#f5f5f5','primaryBorderColor':'#E50914','lineColor':'#E50914','fontFamily':'ui-monospace, monospace','fontSize':'13px'}}}%%
flowchart LR
    A["seed URL<br/>+ max depth"] --> B["CRAWLER<br/>BFS by depth level<br/>hashtable URL dedup"]
    B --> C["page files<br/>URL · depth · raw HTML"]
    C --> D["INDEXER<br/>inverted index<br/>lowercase, len ≥ 3"]
    D --> E["index file<br/>word → docID:count"]
    E --> F["QUERIER<br/>AND binds tighter than OR"]
    F --> G["ranked hits<br/>summed term frequency"]
```

Underneath all three sit four structures I wrote from scratch and reused across the whole course: a bag, a set, named counters that increment instead of erroring on duplicates, and a hashtable of sets for O(1) average lookup. Every `malloc` paired, every NULL input checked, every module clean under valgrind.

<a href="https://github.com/Swabir001/nuggets-group-6"><img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-nuggets.png" width="100%" alt="Nuggets"/></a>

Real-time multiplayer dungeon game over a custom UDP protocol. The server owns everything: map layout, player positions, where the gold is scattered. Clients are terminals that send keypresses and receive live ncurses frames back. Per-player line of sight gets recomputed on every single move, which is where the actual difficulty lives.

<a href="https://github.com/Swabir001/studyPod"><img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-studypod.png" width="100%" alt="StudyPod"/></a>

Match with classmates by course, study style, and availability. Socket.io broadcasts a "studying now" signal to relevant matches, JWT handles auth, and a reliability reputation system means chronic no-shows get filtered out over time rather than wasting everyone's afternoon.

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-apis.png" width="100%" alt="REST APIs on PostgreSQL"/>

Two backends on one foundation, aimed at different problems. A blog platform with full CRUD, and a multiplayer Wordle API managing sessions, guesses, and win/loss state across concurrent games. Schema defined in Prisma, migrations run properly rather than hand-edited, endpoints tested end to end with Cypress.

<a href="https://github.com/Swabir001/swabflix"><img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-frontend.png" width="100%" alt="SwabFlix and Street Food Atlas"/></a>

SwabFlix is a streaming-style interface on live TMDB data: season and episode browsers, watch history, ranked rows, skeleton loading states, responsive down to phone width. Street Food Atlas is a CRUD recipe platform on React Router v7 data mode, where loaders prefetch per route and actions trigger automatic revalidation after writes. Zustand holds the client-only state, including an edit draft so cancelling never destroys the original record.

<!-- ════════════════════════════ 03 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-hardware.png" width="100%" alt="03 Embedded and Hardware"/>

<a href="https://github.com/Swabir001/marble-maze"><img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-marblemaze.png" width="100%" alt="Marble Maze"/></a>

A physical tilt-to-navigate LEGO maze on an STM32C031C6TX. Joystick ADC drives two NEMA steppers to tilt the platform, an I²C display counts down thirty seconds, and interrupt-driven sensors on PA5/PA6 catch the finish line. The real design work was the four-state machine and a 200-unit ADC deadzone, tuned to kill joystick jitter without making the controls feel dead. Interrupt architecture instead of polling kept motor response under 10ms.

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-fpga.png" width="100%" alt="FPGA Neural Network Accelerator"/>

Rather than running inference in software, I synthesized it into logic. C with HLS annotations went through Vitis HLS into RTL, then into Vivado alongside the ARM core, connected over AXI. I wrote the driver on the processor side and ran co-simulation to prove hardware and software agreed on every test vector. Then I optimized and tracked what happened: loop unrolling, `PIPELINE II=1`, AXI Stream for continuous feed, with latency, initiation interval, and LUT/FF/BRAM/DSP usage logged at every step. The lesson was watching the bottleneck migrate off the accelerator and onto memory bandwidth.

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-baremetal.png" width="100%" alt="Bare-metal ARM"/>

Everything that happens before `main()` is called. Startup code copying `.data` from flash into RAM, zeroing `.bss`, setting the stack pointer, laying out the interrupt vector table. Custom linker scripts placing code and data exactly where I wanted them, and C and assembly calling into each other. Then I stripped floating point out of a neural network entirely, because cheap microcontrollers emulate float in software and pay dearly for it: float32 weights quantized to int8 with scale factors, sigmoid swapped for a lookup table. Same predictions, a fraction of the flash and cycles, measured both ways rather than assumed.

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-tinyml.png" width="100%" alt="TinyML and SPI"/>

Human activity recognition, full lifecycle on real silicon. I collected three-axis motion data over SPI, trained a classifier in Python, converted the weights to C arrays, deployed inference on the STM32, then measured accuracy against latency and memory footprint on the actual chip. That last step is the one most ML coursework skips. The accelerometer driver is interrupt-driven rather than polled, so the chip raises an interrupt when data is ready and the CPU touches it only then. Separately I programmed an ESP32-C3 as a BTLE-to-UART bridge, so a plain serial device goes wireless without knowing BTLE exists.

<!-- ════════════════════════════ 04 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-coursework.png" width="100%" alt="04 Coursework"/>

<details>
<summary><b>&nbsp;CS50 · Software Design & Implementation &nbsp;<code>C · systems</code></b></summary>
<br/>

No garbage collector, no frameworks, no hand-holding. Everything designed, implemented, tested, and documented.

**Data structures from scratch.** Bag as a manually managed linked list. Set as a string-keyed store with no duplicates. Counters, where inserting an existing key increments rather than errors. Hashtable as a fixed array of sets with a hash function mapping keys to buckets. Unit test drivers and regression scripts for each, then reused throughout the projects above.

**Tiny Search Engine.** Crawler, indexer, querier as three piping programs. Detailed in section 02.

**Nuggets.** 26-player UDP game server and clients. Detailed in section 02.

**Collaborative graphical editor.** Multi-threaded Java client-server drawing tool where multiple clients edit one shared canvas.

`linked lists` `hash functions` `dynamic allocation` `function-pointer iterators` `defensive programming` `modular headers` `valgrind`

</details>

<details>
<summary><b>&nbsp;CS52 · Full-Stack Web Development &nbsp;<code>React · Node · Postgres</code></b></summary>
<br/>

Started at raw HTML and CSS, added one layer of the stack per assignment.

**Responsive landing page.** Semantic HTML and Flexbox, debugged live in DevTools. Learning how browsers actually lay out and paint a page.

**Async DOM quiz.** A "what city should you live in" personality quiz in jQuery. Questions in a JSON file loaded asynchronously, which meant handling callback ordering so the DOM was ready before populating it. Deployed static on Render.

**Notes app.** First React project. Components, props flowing down, state triggering re-renders, callbacks handed to children.

**Street Food Atlas.** React Router v7 data mode with loaders and actions, Zustand for client-only state. Detailed in section 02.

**Blog API and Wordle API.** Express, Prisma, PostgreSQL, Cypress. Detailed in section 02.

**SwipePlate.** Final project, two repos, real users. Detailed in section 02.

`DOM & events` `async JSON` `component composition` `loaders/actions` `ORM migrations` `E2E testing` `deployment config`

</details>

<details>
<summary><b>&nbsp;ENGS 62 · Microprocessors in Engineered Systems &nbsp;<code>embedded C · ARM · FPGA</code></b></summary>
<br/>

Programming computers at the hardware level: processor architecture, peripherals, memory layout, then designing custom accelerators.

**Bit manipulation and QEMU workflow.** Hex arithmetic, shifts and masks to set, clear, and toggle individual register bits, function pointers. Cross-compile for ARM and run in emulation for fast iteration before touching real chips.

**Neural network in C on a microcontroller.** Trained XOR in Python for the weights, then reimplemented the forward pass in C by hand: multiply, bias, sigmoid, threshold. First contact with TinyML.

**ARM assembly and bare-metal startup.** Thumb instructions directly, fetch-decode-execute, registers and stack, then linker scripts and the full pre-`main()` sequence.

**Quantization.** Same network with all floating point removed, measuring code size, RAM, and execution time both ways.

**BTLE bridge, SPI driver, activity recognition, FPGA accelerator, HLS optimization.** All detailed in section 03.

`register-level C` `cross-compilation` `Thumb asm` `linker scripts` `fixed point` `SPI/USART/ADC` `HLS` `AXI` `pipelining vs resources`

</details>

<details>
<summary><b>&nbsp;Everything else on the transcript</b></summary>
<br/>

| course | what it covered |
|---|---|
| **CS10** · [repo](https://github.com/Swabir001/cs10-java-oop-data-structures-and-algorithms) | Java OOP, data structures, graph search, client-server, multithreading. I now TA this course. |
| **COSC 61** · Database Systems | Relational modelling, SQL, query planning, normalization. |
| **ENGS 28** · Embedded Systems | STM32 firmware, GPIO, UART, SPI, I²C, ADC, interrupt architecture. TA'd it the following term. |
| **ENGS 31** · Digital Electronics | VHDL on Basys 3, K-map minimization, FSM design, SPI transmitter, ripple-carry adder, digital combination safe. |
| **ENGS 20** · Scientific Computing | MATLAB, numerical methods. |
| **ENGS 21 / 22 / 23 / 25 / 30** | Engineering design, systems, distributed systems, thermodynamics, biological physics. |
| **MATH 8 / 13 / 14 / 22 / 23** | Multivariable calculus, linear algebra, differential equations. |
| **PHYS 13 / 14 · CHEM 5** | Mechanics, electricity and magnetism, general chemistry. |

</details>

<!-- ════════════════════════════ 05 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-stack.png" width="100%" alt="05 Stack"/>

<div align="center">

<img src="https://skillicons.dev/icons?i=c,cpp,python,java,ts,js,react,nextjs,nodejs,express&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=firebase,mongodb,postgres,tailwind,docker,git,linux,bash,cmake,vscode&theme=dark" />

</div>

```
LANGUAGES    C · C++ · Python · Java · TypeScript · JavaScript · SQL · ARM Thumb asm · VHDL
WEB          React · Next.js · Node · Express · Prisma · Firebase · Postgres · Mongo · Tailwind
EMBEDDED     STM32 · Cortex-M0+/M4 · FreeRTOS · SPI/UART/I²C · ADC/PWM/GPIO · BTLE · ESP32-C3
FPGA / ML    Vitis HLS · Vivado · AXI Stream · TensorFlow · scikit-learn · int8 quantization
TOOLING      Git · Docker · GDB · Valgrind · QEMU · Cypress · JTAG/SWD · logic analyzer · SolidWorks
```

<!-- ════════════════════════════ 06 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-research.png" width="100%" alt="06 Research"/>

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/card-pedot.png" width="100%" alt="PEDOT:PSS implants"/>

Standard PEDOT:PSS-on-gold implants delaminate under cyclic stimulation, so the goal is removing the metal interface entirely. I run the fabrication workflow — photolithography, spin-coating, parylene-C CVD, RIE — and characterize with EIS and CIC testing across repeated stimulation cycles. Regenerative Bioelectronics Lab, supervised by Prof. Alex Boys. Manuscript in preparation.

|  |  |
|:--:|:--|
| 🏆 | **2024 Louis J. Setti International Intern Award**, for the E.E. Just research placement |
| 📄 | **Co-author**, 45th SICOT Orthopaedic World Congress, Spain 2025 — global participation in pediatric hand surgery |
| 🎓 | **E.E. Just Undergraduate Fellow** · **FYSEP STEM Academic Fellow** |
| 🇰🇪 | **KenSAP Coding Instructor** — taught Python to Kenyan scholars headed to US universities |

<!-- ════════════════════════════ 07 ════════════════════════════ -->

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/hdr-offclock.png" width="100%" alt="07 Off-clock"/>

<table>
<tr>
<td width="33.3%"><img src="https://raw.githubusercontent.com/Swabir001/portfolio/main/images/photo-buggy.jpg" width="100%"/></td>
<td width="33.3%"><img src="https://raw.githubusercontent.com/Swabir001/portfolio/main/images/photo-desert.jpg" width="100%"/></td>
<td width="33.3%"><img src="https://raw.githubusercontent.com/Swabir001/portfolio/main/images/photo-boat.jpg" width="100%"/></td>
</tr>
</table>

Badminton, swimming, and whatever New Hampshire has open for hiking. I once lost an embarrassing amount of time to the question of why a cow is called a cow and not a goat. Who made that sound first, and why did everyone else go along with it. My friends tolerate this. It's also exactly why I'm decent at root cause analysis.

<div align="center">

&nbsp;

<img src="https://raw.githubusercontent.com/Swabir001/Swabir001/main/assets/rule.png" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=700&size=24&pause=1300&color=E50914&center=true&vCenter=true&width=640&height=48&lines=if+you're+hiring%2C+let's+talk." alt="cta"/>

[![contact](https://img.shields.io/badge/swabir.m.bwana.27%40dartmouth.edu-E50914?style=for-the-badge&labelColor=0A0A0A)](mailto:swabir.m.bwana.27@dartmouth.edu)

&nbsp;

</div>
