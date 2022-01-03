# Notes

**Topic**: The "Solarwinds" attack and farm-to-table methods in the development process - Mitigating disasters through supply-chain security

## Sources

```bibtex
@techreport{sherman2019risks,
    title={Risks in the software supply chain},
    author={Sherman, Mark},
    year={2019},
    institution={CARNEGIE-MELLON UNIV PITTSBURGH PA PITTSBURGH United States}
}

@inbook{inbook,
    author = {Zomer, Gerwin},
    year = {2019},
    month = {08},
    pages = {575-592},
    title = {Supply Chain Security},
    isbn = {978-3-319-92446-5},
    doi = {10.1007/978-3-319-92447-2_25}
}

@unknown{unknown,
    author = {Chaudhary, Sunil},
    year = {2021},
    month = {05},
    pages = {},
    title = {Supply chain security recommendations 1}
}

@article{article,
    author = {Ellison, Robert and Goodenough, John and Weinstock, Charles and Woody, Carol},
    year = {2022},
    month = {01},
    pages = {},
    title = {Evaluating and Mitigating Software Supply Chain Security Risks}
}

@article{article,
    author = {Hassija, Vikas and Chamola, Vinay and Gupta, Vatsal and Jain, Sarthak and Guizani, Nadra},
    year = {2020},
    month = {10},
    pages = {},
    title = {A Survey on Supply Chain Security: Application Areas, Security Threats, and Solution Architectures},
    volume = {PP},
    journal = {IEEE Internet of Things Journal},
    doi = {10.1109/JIOT.2020.3025775}
}

@article{article,
    author = {Alsabbagh, Bilal and Kowalski, Stewart},
    year = {2015},
    month = {07},
    pages = {30-39},
    title = {A Socio-technical Framework for Threat Modeling a Software Supply Chain},
    volume = {13},
    journal = {IEEE Security & Privacy},
    doi = {10.1109/MSP.2015.72}
}

@inproceedings{TorresArias2019intotoPF,
    title={in-toto: Providing farm-to-table guarantees for bits and bytes},
    author={Santiago Torres-Arias and Hammad Afzali and Trishank Karthik Kuppusamy and Reza Curtmola and Justin Cappos},
    booktitle={USENIX Security Symposium},
    year={2019}
}

@article{9473230,
    author = {J. Viega and J. Michael},
    journal = {Computer},
    title = {Struggling With Supply-Chain Security},
    year = {2021},
    volume = {54},
    number = {07},
    issn = {1558-0814},
    pages = {98-104},
    keywords = {industries;government;risk management;computer security;supply chain management},
    doi = {10.1109/MC.2021.3075412},
    publisher = {IEEE Computer Society},
    address = {Los Alamitos, CA, USA},
    month = {jul}
}
```

**Socio-technical Framework for Threat Modeling a Software Supply Chain**

- Software supply chains are similar to traditional supply chains
- A supply chain is created by deploying and using a product directly or reproducing it as a new product in repetition
- Traditional supply chains can have risks
  - Late product delivery
  - Counterfeits
  - Human errors
- Software supply chains have risks too, i.e. faulty code (intentional or unintentional)
- Risk management is used to counteract these known vulnerabilities
- The first step is to create a threat model of the system
- Threat models must not be too complex in order to be useful
- Current practices in supply chain security
  - Classical CIA triad: Confidentiality, integrity, availability
  - Some newer ones: Possession, authenticity, utility
  - Specific to supply chains: Confidentiality, data integrity, source authenticity, availability, non-repudiation
  - NIST publishes best practices for securing a supply chain, but not concrete recommendations
- Thread modeling requires two processes: Modeling the system and modeling threats to the system
- Software systems and supply chains cannot be viewed as purely technical or social systems, but only as a combination of the two (a "sociotechnical" system)
- ISO 27005: A threat is a potential cause of an incident that might result in harm to systems and organizations
- Threat modeling systems should express and capture as many threats as necessary
- Actual threats: Intention, capability and opportunities, potential threats might miss one
- Both types of threats must be found, as potential threats can be prevented by acting early
- Supply chain vulnerabilities can be found by analyzing the relations of the integrated elements that compose each threat in the system
- The sociotechnical framework is based on two models/systems: A dynamic model of sociotechnical changes ("sociotechnical system") and a static model ("security by consensus")
- The social subsystem contains culture (collection of values) and structure (distribution of power)
- The technical subsystem contains methods (techniques) and machines (technical artifacts)
- All four subsystems \*culture, structure, methods, machines) determine the security state of the system
- If one part of the system changes, the other parts must adapt (i.e. new, younger managers)
- The security by consensus system defines a few layers: ethical, political and legal, administrative and managerial, operation, application, operating system, hardware
- Both internal and external changes (social or technical) will affect security, so measures need to be deployed systematically
- Security frameworks make it possible to analyze supply chain security using the individual layers (vulnerabilities in one layer might for example be mitigated by another)
- By looking at software supply chains as interconnected sociotechnical systems reviewers can verify that the layers across the systems are secured similarly
- Comparing the different layers of the individual supplier's sociotechnical systems allows for creating a chain of (dis-)trust, where for example the usefulness of digital signatures for the compiler binaries is negated by compiling unsigned source code or not checking the provided binaries' signatures
- Six processes need to be analyzed: Supplier sourcing, software development and testing, software packaging, product delivery through network or software product manufacturing & physical software product delivery - this can be done by analyzing the products which are being sent between the different processes
- Supplier sourcing and product delivery link companies together, which often leads to generic processes like software packaging
- FLOSS and COTS software are transmitted from supplier sourcing to software development and testing processes, including related secrets and vulnerability information
- In the delivery process, four or five elements (secrets, vulnerabilities, source package and/or binary package, user guide) are sent to the user (over the network or physically)
