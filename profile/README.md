# About

Axini helps deliver complex software products on time without concessions on quality. Our unique testing platform gives early insights in potential issues and prevents surprises late in the project. This approach is based on more than 30 years of academic research and is proven to work at ProRail, Achmea and Thermo Fisher Scientific. This way, reliable software is guaranteed, no matter how complex.

Visit our <a href="https://www.axini.com">website</a>, follow us on <a href="https://www.linkedin.com/company/axini">LinkedIn</a> or <a href="https://www.axini.com/contact">contact us</a> for more information.

## Plugin adapter

Our repositories contain example code for *plugin adapters* required to connect the Axini Modeling Platform (AMP) to the system under test.

Plugin adapter connect to AMP using a <a href="https://en.wikipedia.org/wiki/WebSocket">WebSocket</a> connection and communicate using our dedicated *plugin adapter protocol*. The following images shows an overview of the states and messages of the protocol.

<img src="https://github.com/Axini/.github/assets/164359185/f0299e5d-e369-40f0-ac71-aa82051e6c57" alt="Overview of the plugin adapter protocol.">

The messages of this protocol are defined using the language independent <a href="https://protobuf.dev">Google Protocol Buffers</a>. The official Protobuf tools can generate code for many programming languages. The `*.proto` schema files describing the message structure can be found in the <a href="https://github.com/Axini/plugin-adapter-protocol">plugin adapter protocol repository</a>.

The example plugin adapters follow our in-house architecture. It aims to separate concerns and maximize reuse. As a result, many of the components can be reused in your own plugin adapters. The components that communicate with the system under test are domain specific. In the example plugin adapters, the domain specific parts are customized for our *SmartDoor* example system. The following image shows the components of the plugin adapter.

<img src="https://github.com/Axini/.github/blob/main/profile/plugin_adapter_architecture.png" alt="Overview of the plugin adapter components.">

The *Effective AML documentation* available in AMP contains more information on plugin adapters, the protocol and our architecture.
