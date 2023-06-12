---
layout: page
title: MazeRunners
description: a multiplayer maze solving game using an fpga as a controller!
img: /assets/img/maze_runners_bg.jpg
importance: 1
category: work
---

<a href="https://github.com/Zsombito/infoprog-cw">Repository link</a>.

As a member of a team of six, we successfully designed and developed a multiplayer game using Unity, featuring a unique twist — a custom controller built around an FPGA. The game revolves around players navigating a maze with the ultimate goal of reaching the centre first, providing an engaging and competitive experience.

<div class="row">
    <div class="col-sm">
        {% include figure.html path="assets/img/maze_runners_wizard.jpg" title="wizard" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.html path="assets/img/maze_runners_orc.jpg" title="orc" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.html path="assets/img/maze_runners_cowboy.jpg" title="cowboy" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.html path="assets/img/maze_runners_nerd.jpg" title="nerd" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Choose your character! From left to right we have the Wizard, Orc, Cowboy and Geek.
</div>

My primary role within the team was to design the FPGA-based controller, which served as a hardware interface for the game. The controller had an onboard accelerometer, buttons, and switches, allowing players to interact physically with the game environment. Leveraging the FPGA's capabilities, I implemented various signal filtering techniques to process the accelerometer data in hardware, ensuring precise and responsive control.

The FPGA, acting as the controller's core, generated control signals based on the processed accelerometer data. These control signals were then transmitted to a Python-based software backend. The Python code communicated with the game client on the player's local device, providing essential information for enacting the player's actions within the game. These actions encompassed movements, speed modifiers, and even the ability to shoot projectiles. The local client would then communicate with an external server, which consolidated player data and fed-back responses to update each player's local client. Due to lack of processing power, an event-driven system was not feasible since the system could not sustain enough events per second. Hence, the method we chose was a polling-based system whereby the server would periodically poll the players for their game information.

One of the notable technical successes of this project was the effective utilization of hardware-based data processing. By implementing the accelerometer data processing on the FPGA, we achieved exceptional performance without compromising responsiveness. The game's speed was ingeniously linked to the FPGA's accelerometer reading, allowing players to control their in-game character's movement speed by manipulating the FPGA's movement speed. This synchronization between real-world movements and in-game actions added an immersive layer of gameplay dynamics.

The seamless integration of the FPGA-based controller, Python backend, and Unity game engine demonstrated our team's ability to work across diverse technical domains. This successful integration was the result of meticulous collaboration, efficient communication, and a solid understanding of both hardware and software components.

Our project showcased the potential of FPGA technology in enhancing gaming experiences. By designing a custom controller and leveraging FPGA hardware capabilities, we provided players with a unique and immersive gameplay experience, elevating their level of engagement and enjoyment.

<div class="row">
    <div class="col-sm">
        {% include figure.html path="assets/img/mazerunners_arch.jpg" title="mazerunners arch" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The simplified architecture of the system.
</div>

In summary, the multiplayer maze game with an FPGA-based controller project exemplifies our team's technical expertise, collaborative skills, and innovative thinking. It highlights our ability to combine hardware and software components seamlessly to create an interactive and immersive gaming experience. The project stands as a testament to our team's creativity and proficiency in leveraging cutting-edge technologies to push the boundaries of gaming.


