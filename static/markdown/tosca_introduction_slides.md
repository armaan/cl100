# Introduction to TOSCA

Welcome to the Cloudify Demo!  We'll begin with an overview of the TOSCA
template language.

![image](/asset-v1:cloudify+cl100+{{ RUN }}+type@asset+block@images_cloudify_logo.png)

To move to the next slide, press the SPACEBAR or the DOWN ARROW key.
<!-- .element: style="text-align: center" -->


## What is TOSCA?

**TOSCA**, short for Topology and Orchestration Specification for Cloud
Applications, is a template language developed recently by OASIS, a standards
organization, to describe the topology of a cloud.

TOSCA 1.0 was approved in early 2014, a project sponsored by leading companies
such as IBM, RedHat, Huawei, and others.  Its goal is to provide a
platform-agnostic orchestration tool for cloud administrators, one that can
describe any topology, workflow, and policy across different cloud
implementations:

![image](/asset-v1:cloudify+cl100+{{ RUN }}+type@asset+block@images_tosca_overview_1.svg)


## TOSCA Simple Profile in YAML

The original TOSCA specification describes an XML DSL, or Domain Specific
Language.  Luckily, though, the TOSCA Simple Profile in YAML 1.0 is in the
final stages of approval.

YAML is a more human-friendly language than XML, with a syntax much easier to
read and edit.  Thus, the TOSCA Simple Profile in YAML version aims to be more
accessible and concise, not least of which to speed the adoption of TOSCA
itself.

You can find Draft 05 of the Simple Profile specification
[here](http://docs.oasis-open.org/tosca/TOSCA-Simple-Profile-YAML/v1.0/csprd02/TOSCA-Simple-Profile-YAML-v1.0-csprd02.html).


## TOSCA Relationship Diagrams

But it's not just XML and YAML.  In order to describe any application in TOSCA
terms, you can draw a diagram like this:

![image](/asset-v1:cloudify+cl100+{{ RUN }}+type@asset+block@images_tosca_overview_3.svg)

This diagram has 5 **nodes**, represented by square boxes.   Nodes in a
topology are components of the topology, not physical or virtual computers.
Every node has a name and a type, the latter of which we'll discuss in a
subsequent chapter.

Nodes also have relationships with each other: connections and containment.
You can see both of these types of relationships in the diagram as well.  The
ones of type "Contained-In" are implicit, where one node is contained in
another, whereas "Connected-To" are explicit, wherever arrows are drawn.


# End of Unit
Please click on the right arrow below to move on to the next unit.
<!-- .element: style="text-align: center" -->
