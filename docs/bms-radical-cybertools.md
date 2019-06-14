---
id: bms-radical-cybertools
title: RADICAL-Cybertools
---

* Name: **RADICAL-Cybertools**
* License: [MIT](https://github.com/radical-cybertools/radical.pilot/blob/devel/LICENSE.md)
* Home page http://radical-cybertools.github.io/
* Source code: http://github.com/radical-cybertools/

## Summary

RADICAL-Cybertools are a set of software modules that can be used independently, composed into a single system, or integrated into existing systems to extend their functionalities. RADICAL-Cybertools specifically targets High Performance Computing (HPC) machines to enable the execution of scientific workflows from diverse scientific domains. RADICAL-Cybertools are built in Python, and as such are easily deployable into user space.

## Purpose and Capabilities


[RADICAL-Cybertools](https://radical-cybertools.github.io/) are a set of software modules that allow the definition, and execution of workflows as well as workloads. 

[RADICAL-Ensemble Toolkit](https://radicalentk.readthedocs.io/en/latest/) (RADICAL-EnTK), part of RADICAL-Cybertools, is a workflow engine, exposing an API for the description of scientific applications in terms of static or dynamic workflows. RADICAL-EnTK defines pipelines, stages, tasks, and resources. Pipelines are sequences of stages that, in turn, are sets of tasks. Resources are acquired and managed via a third-party runtime system. Tasks are executed by that runtime system on the acquired resources.

[RADICAL-Pilot](https://radicalpilot.readthedocs.io/en/latest/) is a pilot system that exposes an API to enable the acquisition of resources on which to schedule workloads for execution. The design of RADICAL-Pilot includes pilot and compute unit as entities. Capabilities are made available to describe, schedule, manage and execute entities. Pilots, units and their functionalities abstract the specificities of diverse types of resource, enabling the use of pilots mainly on single and multiple HPC machines, but also on HTC and cloud infrastructures. A pilot can span single or multiple compute nodes, resource pools, or virtual machines. Units of various size and duration can be executed, supporting MPI and non-MPI executables, with a wide range of execution environment requirements.

## Who uses it?

The audience of such our tools are application or middleware developers who want to be able to use High Performance Computing Resources to run an ensemble of tasks. Our use cases span from Molecular Dynamics simulations, climate and earthquake simulation, to imagery analysis for Geosciences.

Our system typically supports applications that require to use hundreds or thousands of cores concurrently on HPC resources


## References
1. RADICAL-Cybertools: https://radical-cybertools.github.io/
2. Building Blocks for Workflow System Middleware. M. Turilli, A. Merzky, V. Balasubramanian, S. Jha. Proceedings of the 18th IEEE/ACM International Symposium on Cluster, Cloud and Grid Computing (CCGrid).
