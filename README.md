# Circomy

    A protocol specification for circular economy data and finance using self-sovereign identity

## Abstract

   This document contains a protocol specification for collecting, curating, and indexing circular economy specific data. The technology used is self-sovereign identity, decentralized identifiers, and verifiable credentials for large scale, unpermissioned asset tokenization with or without blockchain technology.

   The following use cases are guiding examples, while others may also be applicable:

   1. Support sharing, as-a-service and performance-based scenarios where goods, materials, or other assets require capital investment so that they can be more easily moved out of the originating balance sheet. In broad terms, this means securitization. As examples: A motor company that would lease motors instead of selling and having the lease contracts in commercial special purpose vehicle thus easing their capital requirements and with the overall effect of equipment used at full capacity and fewer pieces needed. Or bundling micro-financed assets into securities. Or "paying for ecosystem services" (e.g., protective wetlands).

   2. Turning existing materials in circulation to certificated stock or other larger, reusable pieces. Examples being concrete, metals, and larger pieces such as load-bearing structures in the built environment or nutrients flow scenarios.

   3. Project finance in general and in nature-based (and water) adaptation projects in particular but also impact projects.

   4. Signing, collecting, and linking data so it can be used as a basis in environmental, social, and governance (ESG) reporting and life cycle assessment (LCA) like reporting. As an example collecting Internet of Things (IoT) water data from metering and water facilities and having local businesses, such as factories or hospitality establishments, basing their ESG reporting on that. In this case, such reporting could drive change towards closed-loop water circulation, thus creating circular water economies. Data is also applicable to securitization, such as mentioned in bullet 1., and with bullets 2. and 3. one particular framework of application is urban metabolism accounting.

   5. Supporting a systemic impact evaluation. Impact evaluation is critical because it examines and brings new methods to use while ESG deals with more backward-looking, historical data. Impact evaluation has the potential to bring existing academic and industrial expertise into the real economy, consequently scaling finance-related due diligence and providing systemic methods to map towards new, environmentally, and socially beneficial use cases adapted into the local environment.

   Decentralized identifiers and verifiable credentials are a low-cost method to link documents that support large scale, decentralized, unpermissioned asset tokenization in current "business as usual" setting. At the same time, they provide valuable information to direct capital to sustainable causes and bring currently external factors closer to contemporary (ESG) accounting with the associated benefits of accounting. This offers the opportunity to create and link in discoverable fashion life cycle assessment (LCA) data, so that is broadly useable in the economy while providing support especially to small and medium (SME) business financing to realize already known business models and maybe even new business models in the future (e.g., based on "tagging" and sharing IPR and revenue).

   The core protocol defines a data, and a coordination framework using the goal uses cases to transition from the current linear economy to a circular or green, sustainable economy. Another framing is Sustainable Development Goals by the United Nations. The intended audience also includes the financial sector, policymakers, researchers, as well as business professionals and third party programmers. As such, this document explains briefly core concepts to establish a standard frame to encourage discussion on the enabling use cases to realize sustainable development goals and circular economy. The explanations besides the technical specification presented are not exhaustive, refer to external material, and while the term "circular economy" is used, existing criticism of the most commonly used definitions is noted.

   In circular economy materials circulate in closed loops, energy is from renewable sources, and social inclusion is implicit. In a business setting, waste and pollution are designed out, products and materials are kept in use most efficiently, and business models move more onto cooperative and service-oriented models. Financially, negative externalities are revealed and allocated appropriately, leading to natural regenerative systems. The current economy is a linear one, the transition to a circular economy needs to be a systemic requiring concerted action by stakeholders in businesses, government, civil society, finance as well by innovators and scientists. Decentralized identifiers and verifiable credentials can be used to create an auditable, open-ended data framework that supports this transition by cataloging and ranking the data, facilitating cooperative business models, scientific discoveries, and sustainability linked projects, consequently creating a pipeline of green investment assets while also cooperatively deterring greenwashing. This document introduces the rationale to use decentralized identifiers and verifiable credentials in this context, some specific considerations and use cases.

## Status of This Memo

   Draft.  

## Copyright Notice

   Copyright (&copy;) Lumoin (2020).

## 1. Introduction

A commonly used definition of "circular economy" is given by Ellen MacArthur Foundation at [What is the circular economy](https://www.ellenmacarthurfoundation.org/circular-economy/what-is-the-circular-economy) stating

> A circular economy is based on the principles of designing out waste and pollution, keeping products and materials in use, and regenerating natural systems.

While the site explains the circular economy in more detail, this particular definition is occasionally criticized as being an engineering solution, whereas a more comprehensive approach could be needed. A few recent, prominent articles appeared in [Green Economy Coalition](https://www.greeneconomycoalition.org/) blog [Circular economy isn't enough](https://www.greeneconomycoalition.org/news-analysis/circular-economy-isnt-enough-we-need-system-change) (formerly at Smart CSOs Lab [The circular economy cannot achieve its aims without deeper system change](https://www.smart-csos.org/blog-on-theory-and-practice/the-circular-economy-cannot-achieve-its-aims-without-deeper-system-change)) and [P2P Accounting for Planetary Survival](http://commonstransition.org/p2p-accounting-for-planetary-survival/) by [P2P Foundation](https://p2pfoundation.net/) for instance argue for a more comprehensive approach. One reason mainly is that concentrating on reduced resource consumption and extended product life-cycles induces [Jevons paradox](https://en.wikipedia.org/wiki/Jevons_paradox) where cheaper production costs translate to more sales and hence more consumption. We note a reduction in resource consumption is removing slack in optimization terms, and businesses already do this as part of their planning processes. Hence efficient means to reduce slack within companies can become a suitable catalyst to induce a business chance. Overall, there are more than 100 different definitions for the circular economy, as noted in [What is the definition of a circular economy](https://kenniskaarten.hetgroenebrein.nl/en/knowledge-map-circular-economy/what-is-the-definition-a-circular-economy/) but the differences are usually in the focus or scope. Specifically, in this document, the focus is on the financial system, engaging it, and drive change through it.

To create a profound impact on the financial system is vital because it allocates resources and coordinates the broader economic activity. A critical catalyst is a well-documented shortage of green investment assets (e.g. [ESG: green bonds have a chicken and egg problem](https://www.euromoney.com/article/b1fxdsf5kpjxlg/esg-green-bonds-have-a-chicken-and-egg-problem), [ESG: A responsible investment' wishlist' for 2019](https://www.ipe.com/esg-a-responsible-investment-wishlist-for-2019/10028764.article)) and the introduction of [EU Sustainable Finance Taxonomy](https://ec.europa.eu/info/publications/sustainable-finance-teg-taxonomy_en) &ndash; "GDRP of Finance" in IT terms &ndash; and the [EU Green Deal](https://www.euractiv.com/section/energy-environment/news/eu-seals-deal-on-green-finance-in-breakthrough-for-climate-goals/) can be argued to increase demand for green assets further; that is, addressing this imbalance of demand and supply is in favor of sustainability transition. However, [Basel III](https://www.bis.org/bcbs/basel3.htm) regulations will tighten capital adequacy ratio rules for financial institutions. For a sustainability transition, this is a problem because they are not well-tried or, for example, their operational expenses are likely more complicated compared to currently widely used methods, thus making them more challenging to finance (due to perceived risk). Some cross-cutting problems in financing circular business models can increase counterparty risks due to more parties, reporting, and transaction costs. In sum, the accounting rules, relative illiquidity of green finance markets, financing risks, and other market structure issues, capital flow to sustainable causes is likely reduced. The solution to capital adequacy ratio problems may also present a solution in how to move the circular economy and hence would be desirable to financial institutions. This could also mean initial action is well known and doable while [transition risks](https://www.caixabankresearch.com/en/climate-change-green-transition-and-financial-sector) (see the image for clarification) can be still handled.

The change needs to be coordinated in a globally connected world when most of the enterprises participating in the economy are small, and medium (SME) sized. For example, according to Eurostat [Statistics on small and medium-sized enterprises](https://ec.europa.eu/eurostat/statistics-explained/index.php/Statistics_on_small_and_medium-sized_enterprises) 99% are such enterprises in Europe. From a systemic, financial supply-chain perspective, larger companies pushing increasing reporting obligations further in the supply chain, thus increasing costs without appropriate financing or increased cash-flow is a difficult issue. So it would be essential to enhance the ability to report and reduce transaction costs so that the opportunity costs for banks would favor more circular or sustainable credit lines instead of "standard" SME finance or mortgage or retail banking. This would likely enhance sustainability project appraisal and equity investment capability.

An in-depth discussion of global financial system problems and how to innovate as part of supply-chains are not in the scope of this introduction. These could be very well specific business innovations.

### 1.1 Problem Statement

For the problem context in this specification [Accelerating the transition to the circular economy: Improving access to finance for circular economy projects](https://op.europa.eu/en/publication-detail/-/publication/21a71687-ee30-11e9-a32c-01aa75ed71a1) poster is used to introduce a concise set of point, while also noting the [the report the poster](https://op.europa.eu/en/publication-detail/-/publication/02590134-4548-11e9-a8ed-01aa75ed71a1) is based on.

1. Lack of a level playing field for circular economy businesses.
2. Insufficient value-chain collaboration.
3. Lack of product longevity in business models.
4. Insufficient market participation by consumers.
5. Lack of integration of the costs of externalities.
6. Lack of financial knowledge about the circular economy.
7. Insufficient action by first movers.

Recommendations to the financial sector

1. Develop definitions, taxonomy, and tools to measure an activity's circularity.
2. Analyze the risk of a linear economy and adjust credit risk assessment methods accordingly.
3. Increase the financial sector's awareness and knowledge of the circular economy.
4. Label financial instruments fit for circular economy projects.
5. Establish risk-sharing financial instruments and create a pool of experts.

Recommendations to project promoters

1. Identify circular sources of revenues in an organization and update its strategy.
2. Disclose environmental and social benefits through credible, standardized methods.
3. Take part in collaborative communities of practice to identify opportunities and business partnerships.
4. Increase the capacity of organizations to conceive and implement circular economy projects through training staff.

Recommendations to policymakers

1. Ensure that linear risks are sufficiently evaluated and disclosed.
2. Develop definitions, taxonomy, and benchmarks to measure environmental performance.
3. Establish technical and financial advisory services to support the development of business models.
4. Create favorable framework conditions for circular economy projects through policy actions.
5. Make public authorities act as facilitators for the circular economy.
6. Prioritize financing circular economy investments and businesses through EU financial instruments.

The poster refers further to [The European Investment Bank Circular Economy Guide](https://www.eib.org/en/publications/the-eib-in-the-circular-economy-guide) and [High-Level Expert Group on sustainable finance](https://ec.europa.eu/info/publications/180131-sustainable-finance-report_en).

### 1.2 Proposal

We propose to a decentralized identifier and verifiable credentials to uniquely identify data that can be used in environmental, social, and governance (ESG) reporting, impact analysis, and sustainable finance (e.g., securitization, structured finance, impact finance) after building business-specific tooling. The purpose is to establish an audited trail of data and its reporting that can be referenced by multiple parties, a common source of truth. Explicitly noted:

1. The core data structure should be an envelope that gives an identifier for this kind of an ESG, "impact evidence" or financially relevant data hoisted from industry-specific, semantic data. This way, the financial system can have the data it needs to operate while acting as a conduit for the other supply-chain data. That is, supply-chains are roughly financial, documentation, and physical (logistics) that usually are somewhat joined in ERP or CRM systems. This way, economic data could be more readily linked to operational data while also supporting supply-chain actions. Specifically, this is helpful for [GHG Protocol](http://ghgprotocol.org/) type reporting where corporate value chain emissions are gathered and reported.
2. The protocol should be simple and broadly applicable. It should allow extensions for industry-specific uses cases as it provides for industry-specific data.
3. Implicitly the financial data should be neutral so that it is just held by one or more parties and signed by other parties for stated purposes. So the system use "law as a platform," broadly being compatible with [contracts](https://en.wikipedia.org/wiki/Contract) as understood widely by [conventional law systems](https://en.wikipedia.org/wiki/Legal_origins_theory) specifically concerning documents when they are signed.
4. Base data collection and curation are not free to individuals or organizations and should be rewarded. This is relevant to certain types of nature-based or green-grey projects, for instance.
5. Data and knowledge-intensive products from the data by researchers or engineering companies to new or riskier projects are not free to produce. This may be the case, especially on nature-based on green projects. While applications may be local, the knowledge and products may have global markets. Generating such knowledge requires work and taking risks, so it should be rewarded if used broadly.
6. The framework should allow "green tagging" innovations so innovations in later stages could be "unpermissioned" but pay the source side of supply-chain. So it should allow for IPR and revenue sharing to encourage new circular business models that are not so intimately confined on some supply-chains, and current business models enterprises are part of. Otherwise, it will be challenging to circularize or re-capitalize the circular cycles with innovations.
7. There is considerable uncertainty amongst financing and urban planning community on what works and why and understandable "comic book explanations" of natural, regenerative processes could help to bring clarity. So this sort of education or "storytelling" community could be a decisive factor in making the transition.
8. Many charities and NGOs also collect data and do reports. In some cases, this is a significant burden for local authorities or governments. This may mean there are markets for "transformation products" that create more readily accepted formats out of this.
9. There already exists publicly available environmental data (PAED) that should be included either as linked or otherwise.
10. Since the system is distributed, it should be possible to check if two documents contain the same data.

The issuance and operation of the data hubs and actors should be open-ended so that it does not require permission to join. Reduced transaction costs and availability of data should, in turn, drive coordination capabilities for economic entities and facilitate innovations and software on multiple levels, so everyone has an incentive to work together.

The following sections explain key issues in more detail.

## 2. Data governance

The purpose of this data framework is to support the transition to a circular economy and deepen it using the financial system. The participants in the data framework can be at least in the following roles:

1. **Operators:** Entities that operate the data hub and agents in the network also on behalf of users or proxying access to authenticated data in user systems.
2. **Users:** Entities accessing the data hub and agents in the network. These can be any entities but notably financial institutions, enterprises, public authorities, non-governmental organizations, and individual users.

The operators can be enterprises, trusts, or other parties that are legally allowed to handle the data and the other participants' trust. The core principle of Circomy data framework is adversarial interoperability as defined by [Electronic Frontier Foundation: Adversarial Interoperability](https://www.eff.org/deeplinks/2019/10/adversarial-interoperability)
> competitive, innovative, dynamic marketplace, you need adversarial interoperability: that's when you create a new product or service that plugs into the existing ones without the permission of the companies that make them. Think of third-party printer ink, alternative app stores, or independent repair shops that use compatible parts from rival manufacturers to fix your car or your phone or your tractor.

Permissionless access to the data network means that the framework can grow without undue business or legal costs or risks or coordinated anti-competitive practices by other participants in the system. This access also requires special attention to legal frameworks such as GDPR, appropriate encryption, and electronic signing (e.g. [eIDAS](https://ec.europa.eu/digital-single-market/en/trust-services-and-eid)) technologies.

Many of these issues are currently being discussed. Notable are:

- [EU Digital Single Market Guidance on private sector data sharing](https://ec.europa.eu/digital-single-market/en/guidance-private-sector-data-sharing),
- [Building Trust Through Data Foundations: A Call for a Data Governance Model to Support Trustworthy Data Sharing](https://www.southampton.ac.uk/wsi/enterprise-and-impact/white-papers.page) by **Sophie Stalla-Bourdillon**, **Alexsis Wintour** and **Laura Carmichael** and
- [Web of Trust: Encrypted Data Vaults](https://github.com/WebOfTrustInfo/rwot9-prague/blob/master/final-documents/encrypted-data-vaults.md) by **Amy Guy**, **David Lamers**, **Tobias Looker**, **Manu Sporny** and **Dmitri Zagidulin**.

The following are the main relevant points quoted from Building Trust Through Data Foundations:


>**1. A comprehensive rulebook**

>A data governance model must have a comprehensive rulebook for the usage, sharing, and re-usage of personal and non-personal data, including a robust ethical framework, which should be made publicly available. This rulebook should:
> - Go beyond privacy and data protection compliance and set forth both substantial and process-related safeguards for the whole lifecycle of the data to be shared and (re-)used, that considers the entire data spectrum.
> - Clearly state the objectives of the data sharing and (re-)usage activities to be conducted by the participants, identify critical roles and set workflows and safeguards for decision-making relating to data usage, sharing, and re-usage.
> - Be made publicly available for obvious reasons of transparency and accountability.

> **2. An independent governance body**

> A data governance model must have a strong, independent governance body comprised of independent data stewards with interdisciplinary expertise. The data steward role should be at the core of any data governance model and oversee the decision-making body. This independent governance body should:

> - Help to set up data-sharing arrangements and workflows between key actors.
> - Inform decision-making related to data usage, sharing, and re-usage, and systematically monitor data sharing and data usage practices.
> - Be involved in risk assessment and effective threat modelling. In high risk situations, independent data stewards should be given a whistle-blower role.
> - Commission external roles where appropriate and the necessary authorisation is in place, such as external auditors, to complement their assessment.

> **3. An inclusive decision-making body**

> A data governance model must have a decision-making body that engages participants (in particular data providers) and represents the interests of data subjects. This inclusive decision-making body should:

> - Implement standardised processes that provide meaningful representation of data subjects' interests.
> - Involve data providers in such processes so that they are kept in the loop and adapt their practices over time.

> **4. A standardised process for flexible membership**

> A data governance model must have a standardised process to enable relative flexibility in its membership so that:

> - The structure can smoothly grow overtime without exaggerated (legal) costs.
> - The risks of harm arising through anti-competitive practices are mitigated, e.g. organisations are not excluded from joining a data governance model without reasonable justification.41

> **5. A trust-enhancing technical and organisational infrastructure**

> It is crucial to distinguish between the sharing of data, which should happen through a trust-enhancing technical and organisational infrastructure, and the creation of the legal structure (e.g. through contracts, or the incorporation of a new legal entity). The creation of the legal structure should not automatically lead to data sharing. Data flows should only be triggered once the particularities of each use case are known. Importantly, there is no fundamental opposition between what some have called "the technological model" 42 and the legal model for data sharing.
On the contrary, we suggest that the building of the data governance model, including the selection and refinement of the legal structure, should be informed by current data sharing technological capabilities.
A data governance model must therefore rely upon a trust-enhancing technical and organisational infrastructure, which should:

> - Be able to reduce unnecessary data movements.
> - Tailor the amount of data to specific and legitimate purposes and action the sharing once these purposes have been identified.
> - Monitor queries.
> - Ensure confidentiality through e.g. role-based and purpose-based access control, de-identification solutions including noise injection, multiplication of layers (through federated learning or the "student-teacher" approach), and/or secure multi-party computation depending upon use case.
> - Ensure a high level of accountability through e.g. decentralised solutions such as distributed ledgers or more simply standardised access to data.
> - Provide a level of data security that is adapted to both the sensitivity of the data, and the purpose(s) for its usage, sharing, and re-usage.

> **6. A well-regulated legal structure**

> A data governance model must have a well-regulated legal structure, which should:

> - Represent all stakeholders in decision-making processes, e.g. to give data providers – from start-ups to multinational companies – and data subjects rights and opportunities to voice their opinions regardless of their nature, size, or number.
> - Provide effective authoritative oversight.
> - Have a mature compliance and enforcement function.
> - Be able to manage and examine escalated complaints with recourse to the Courts if required


## 3. Guiding cases

A conclusion of the main enabling technological points and some high-level target cases.

### 3.1 Reporting

Regulations such as EU Sustainable Finance taxonomy and investor demand for green assets create a need for accurate reporting efficiently. In this context, especially environment, social, and governance (ESG) reporting is central, and several proprietary methods are already in use. It should be notable that the underlying data is approximately the same; the means to extract further insight or ways to present the data may be wary.

Plenty of data has been collected and is currently managed, but it may not be directly useable in various reporting purposes without further transformation. While there are now attempts to unify methods and reporting, it takes time and already and will be collected data needs to be transformed. In many cases, data collection is also an expensive and laborious process that should be appropriately rewarded.

Reporting is not a good proxy for technological, environmental, or climate risks as it is backward-looking.

### 3.2 Impact evaluation

Impact evaluation is a set of methodologies to assess the effect of actions taken. Impact evaluation and using the results and learnings are particularly essential to accelerate the pace and quantity of sustainable and impact finance.

To do more than report and help to move into a circular and sustainable economy and building resilience, adapting systems to facilitate brown transition finance and green finance, the framework needs to support methodology to do so. This means (in relevant parts) the saved documents need to define an expectation for monitoring and drawing scientifically valid conclusions. The standards used to support the data need to support CREAM definition, to be **C**clear, **R**elevant, **E**conomic, **A**dequate, and **M**onitorable. Other known acronym for the same purpose is SMART. These documents can be linked to financial objectives and used as a tool to transfer and adapt learning to improve and accelerate adaptation and other project development globally.

### 3.3 Material and energy flow

Material flows and associated energy flows are an important part of a circular economy, especially due to urbanization. For example [Sitra](https://www.sitra.fi/en/) notes in its [material economics](https://www.sitra.fi/en/publications/circular-economy-powerful-force-climate-mitigation/) publication

> circular economy can make deep cuts to emissions from heavy industry: in an ambitious scenario, as much as 296 million tons CO2 per year in the EU by 2050, out of 530 Mt in total – and some 3.6 billion tonnes per year globally. Making better use of the materials that already exist in the economy thus can take EU industry halfway towards net-zero emissions. Moreover, doing so often is economically attractive.

Notably, the markets for recycled construction and demolition waste do not currently function well. This is the case for water and nutrients flows and even electronics, which seem to have some similarities. Rather than try to create "recycling markets" one-by-one, one could create information on in-stock materials (e.g., buildings) and their qualities to make the materials visible and create a price signal. In effect create [certificated stock](https://www.investopedia.com/terms/c/certificatedstock.asp) (example: [Cotton Deliverer's & Receiver's Guide](https://www.theice.com/publicdocs/futures_us_reports/cotton/Cotton_Deliverers_Guide.pdf)) bring them to a merchant trading. This would allow the same financing options as virgin materials, and one could assume recycled materials would be competitive against virgin materials, especially when accounting for life-cycle costs. The materials likely need processing such as concrete on pH or metals to remove impurities. Still, having more information on in-stock quantities, timeliness, and market demand would also allow investing in refineries, logistics. It might introduce demolition and construction innovations throughout the supply-chain if they were financially beneficial.

Some of the issues are also discussed in [Accelerating the transition to the circular economy: Improving access to finance for circular economy projects](https://op.europa.eu/en/publication-detail/-/publication/21a71687-ee30-11e9-a32c-01aa75ed71a1).

#### 3.4 Investing and securitization (and transparency)

The circular economy seems to have more complex counterparty risks (more parties) and more complex operational expenses. It looks almost essential to improve reporting accuracy, timeliness, trustworthiness, and data availability across company boundaries. This should be beneficial even in the current linear economy, also if not explicitly considering the green or circular economy. With improved impact evaluation process, likely more projects will be financed and results and learning transferred to new projects. Reduced transaction costs and improvements in reporting may allow for various impact financing cases to be developed and even business models that are dependent more on dynamic pricing or more complex financing arrangements.

It would be beneficial if the collected data could, at some point, support securitization and due diligence operations. Reducing transaction costs and increasing transparency should increase the liquidity of green assets and their overall desirability. An exciting target case would be to support "circular transparency" through the whole financial chain to derivatives markets. [How to save the world: 1 measure it](https://www.euromoneyconferences.com/article/3771142/how-to-save-the-world-1-measure-it.)

Moreover, an increased supply of green investment assets combined with adding tokenized securitization, should bring other benefits. Such as reduced liquidity and market risk and financing and opportunity costs. More comfortable buying and sell financial assets within the desired time since there are more counterparties at the markets, reducing transaction and search costs, financing, and opportunity costs. These are likely appealing factors in finance and executed correctly should increase capital flows to sustainable causes.
