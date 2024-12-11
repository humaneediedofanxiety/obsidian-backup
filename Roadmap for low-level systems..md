 **Tags |**   #low-level #roadmaps 

-- -
##### **Phase 1: Core Low-Level Concepts**

- **Main Focus**: Learn low-level programming concepts and understand how computers work at the hardware and software level.

- **Daily Learning (3 hours/day)**:

    - Start with **“[[The Hidden Language of Computer Hardware and Software (2000) 2.pdf]]** to get an intuitive grasp of how computers work.
    - Move on to **“The Elements of Computing Systems” (Nand to Tetris)**. Build your own computer system from scratch.
    - Study **C programming** basics alongside, as it’s crucial for systems-level understanding.

- **Side C++ Project (1 hour/day)**:

    **System Monitor Tool**: As you’re learning C and computer systems, build a system monitor that can display the current CPU and memory usage on your Linux system. Use terminal-based libraries like **ncurses** for a text-based UI. This will introduce you to real-time data collection and system calls, which are essential for low-level programming.

##### **Phase 2: Diving Deeper into Low-Level**

- **Main Focus**: Dig into **Assembly Language**, **Computer Architecture**, and Operating Systems.

- **Daily Learning (3 hours/day)**:

    - Study **"The Art of Assembly Language"** to deeply understand how instructions translate at the hardware level.
    - Explore **Operating Systems** by following **“Operating Systems: Three Easy Pieces”**.
    - Start learning **x86 Assembly** and write small programs to strengthen your understanding of how programs execute.

- **Side C++ Project (1 hour/day)**:

    - **File System Tool**: Create a tool that interacts with the file system—read/write files, move files, and delete them using system calls. This will further familiarize you with file handling and C++ interactions with the OS.

    - **Terminal-based Graphics**: Implement a simple **ASCII art** or **text-based visualization** to display system statistics (e.g., CPU load graph, memory usage). Use **ncurses** or **termbox** for terminal graphics, and combine this with the file system tool to display real-time system usage data in a graphical manner.vel.

##### **Phase 3: Advanced Low-Level Topics**

- **Main Focus**: Gain expertise in Operating System Development, Compilers, and Virtualization.

- **Daily Learning (3 hours/day)**:

    - Study **“Modern Operating Systems”** to understand advanced OS concepts like concurrency, memory management, and virtualization.
    - Build a **simple operating system** or kernel module by following tutorials.
    - Start learning about **Compilers** with **“Engineering a Compiler”** and try to implement a tiny compiler or interpreter.

- **Side C++ Project (1 hour/day)**:

    - **Text Editor (like nano)**: Building a basic text editor will help you understand memory management, file handling, and user input/output in real-time. This project can be extended by adding syntax highlighting and implementing more features to refine your understanding of how terminal-based applications interact with the OS.

    - **Terminal-based Game**: A simple terminal-based game (like **Snake** or **Tetris**) can be a great way to apply C++ and terminal graphics. You can use libraries like **ncurses** to handle keyboard input and update the terminal screen dynamically. This project will push you to explore concepts like input buffering, game loops, and optimized real-time rendering.

##### **Phase 4: Synthesis of Low-Level and C++ Skills**

- **Main Focus**: Now, focus on synthesizing everything by building larger, more complex projects.

- **Daily Learning (3 hours/day)**:

    - Take on specialized topics such as **compilers**, **real-time systems**, or **security** depending on your interests.
    - Keep learning advanced C++ features (e.g., **RAII**, **concurrency**, **template metaprogramming**) to enhance your development skills.

- **Side C++ Project (1 hour/day)**:

    - **Game Engine**: Build a minimal game engine in C++ where you handle graphics, user input, and simple physics. You could start by creating a basic 2D game engine using **SDL** or **SFML** and later work your way into more advanced topics like **OpenGL** for graphics and **ECS (Entity-Component-System)** architecture for performance.

    - **Low-Latency Network Library**: If you're interested in networking, create a low-latency network library for real-time communication. Focus on socket programming and multithreading to ensure fast, concurrent data handling.

##### **Additional Terminal Graphics Learning (Ongoing)**

- **Libraries**:

    - **ncurses**: Great for building text-based user interfaces (UIs) in the terminal. You can use it for displaying system stats, menus, or even games.
    - **termbox**: A lightweight, low-level alternative to ncurses that can be used for basic graphics in terminal-based applications.
    - **SDL2**: If you want to move beyond terminal graphics and into more structured graphical apps, SDL2 can provide you with the framework to build 2D graphics applications in the terminal.

---

**References.**
