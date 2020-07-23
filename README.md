# DEVELOPMENT HAS MOVED!

EQEnv is now [Hephaestus-R](https://github.com/QC-at-Davis/Hephaestus-R)! It's still being developed by me but now on behalf of Quantum Computing at Davis (QCaD) 

# EQEnv - the Everything Quantum Environment

Every single Quantum Computing framework/tool crammed into one Docker environment.

## What's Inside
* Jupyter Lab
* IBM Qiskit
* Google Cirq
* Xanadu Strawberry Fields
* D-Wave Ocean
  * `minorminer` - heuristic graph embedding utility
* CQCL Pytket
  * All interfaces included as well: `pytket-qiskit`, `pytket-honeywell`, etc.

### Planned Additions
* Rigetti Forest

## Usage 
Ensure Docker is installed and running in your system.

Copy-Paste the `dockerfile` and `docker-compose.yml` to the directory of your choice.

Then just run:

```
docker-compose up
```

## Development

To force Docker to re-build the image from scratch instead of ignoring the Dockerfile:

```
docker-compose up --build
```

## Why did you build this?

I like to have all of my Quantum Computing tools in one place. Previously, I had a Dockerfile for each tool but I find myself "jumping" across tools or using them in conjunction more frequently than I anticipated.

For example, most frameworks provide a statevector simulator, but I have yet to find one that parallels Qiskit's visualization utilities. I usually find myself taking statevectors and tweaking them so  `plot_bloch_multivector` can display whatever mess I've generated.

Another example is with CQC's `pytket` framework which lets you translate circuits between different frameworks/platforms. I can fire up Qiskit, build something, then pass it through `pytket` to see how Google Cirq might map it.
