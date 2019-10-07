# Circomy

    Decentralized identifier document and protocol specification for circular economy data and finance

## Abstract

   This document contains a technical specification of a decentralized identifier, verifiable credentials and a core protocol which together define a data and a coordination framework with appropriate incentives to transition from current linear economy to a circular or green, sustainable economy. Another framing is Sustainable Development Goals by United Nations. The intended audience includes also people in financial sector, policy makers, researchers as well as business professionals and third party programmers. As such this document explains briefly core concepts to establish a common frame with the goal to encourage discussion on the enabling use cases to realize sustainable development goals and circular economy. The explanations besides the technical specification presented are not exhaustive, refer to external material and while the term 'circular economy' is used, existing criticism of the most commonly used definitions is noted.

   In circular economy is materials circulate in closed loops, energy is from renewable sources and they are socially inclusive. In business setting waste and pollution are designed out, products and materials are kept in use in the most efficient way and business models move more onto cooperative and service oriented models. Financially, negative externalities are revealed and allocated appropriately leading to regenerative natural systems. Current economy is a linear one, the transition to a circular economy needs to be a systemic requiring concerted action by stakeholders in businesses, government, civil society, finance as well by innovators and scientists. Decentralized identifiers and verifiable credentials can be used to create a verifiable, open-ended data framework that support this transition by cataloguing and ranking the data, facilitating cooperative business models, scientific discoveries and sustainability linked projects, consequently creating a pipeline of green investment assets while also cooperatively deterring greenwashing. This document introduces the rationale to use decentralized identifiers and verifiable credentials in this context, some specific considerations and use cases.

## Status of This Memo

   Draft.  

## Copyright Notice

   Copyright (&copy;) Lumoin (2020).

## 1. Introduction

A commonly used definition of 'circular economy' is given by Ellen MacArthur Foundation at [What is the circular economy](https://www.ellenmacarthurfoundation.org/circular-economy/what-is-the-circular-economy) stating

> A circular economy is based on the principles of designing out waste and pollution, keeping products and materials in use, and regenerating natural systems.

While the site explains circular economy in more detail, this particular definition is occasionally critized being an engineering solution whereas a more comprehensive approach could be needed. A few recent, prominent articles appeared in [Green Economy Coalition](https://www.greeneconomycoalition.org/) blog [Circular economy isn't enough](https://www.greeneconomycoalition.org/news-analysis/circular-economy-isnt-enough-we-need-system-change) (originally at Smart CSOs Lab [The circular economy cannot achieve its aims without deeper system change](https://www.smart-csos.org/blog-on-theory-and-practice/the-circular-economy-cannot-achieve-its-aims-without-deeper-system-change)) and [P2P Accounting for Planetary Survival](http://commonstransition.org/p2p-accounting-for-planetary-survival/) by [P2P Foundation](https://p2pfoundation.net/) for instance argue for a more comprehensive approach. One reason particularily is that concentrating on reduced resource consumption and extended product life-cycles induces [Jevons paradox](https://en.wikipedia.org/wiki/Jevons_paradox) where cheaper production costs translate to more sales and hence more consumption. We note reduction in resource consumption is removing slack in optimization terms and businesses already do this as part of their planning processes. Hence efficient means to reduce slack within businesses can be become an efficienty catalyst to induce a business chance. Overall, there are more than 100 different definitions for circular economy as noted in [What is the definition of a circular economy](https://kenniskaarten.hetgroenebrein.nl/en/knowledge-map-circular-economy/what-is-the-definition-a-circular-economy/) but they differences are usually in the focus or scope. Specifically in this document the focus is in the financial system, engaging it and drive change through it.

To create deep impact, financial system is important because it allocates resources and coordinates the wider economic activity. An important catalyst is a well documented shortage of green investment assets (e.g. [ESG: green bonds have a chicken and egg problem](https://www.euromoney.com/article/b1fxdsf5kpjxlg/esg-green-bonds-have-a-chicken-and-egg-problem), [ESG: A responsible investment ‘wishlist’ for 2019](https://www.ipe.com/esg-a-responsible-investment-wishlist-for-2019/10028764.article)) and the introduction of [EU Sustainable Finance Taxonomy](https://ec.europa.eu/info/publications/sustainable-finance-teg-taxonomy_en) &ndash; "GDRP of Finance" in IT terms &ndash; and the [EU Green Deal](https://www.euractiv.com/section/energy-environment/news/eu-seals-deal-on-green-finance-in-breakthrough-for-climate-goals/) can be argued to further increase demand for green assets; that is, addressing this imbalance of demand and supply is in favour of sustainability transition. However [Basel III](https://www.bis.org/bcbs/basel3.htm) regulations will tighten capital adequacy ratio rules for financial insitutions. For a sustainability transition this is a problem because sustainable business models are not well tried or for example their operational expenses are likely more complicated compared to currently widely used methods, thus making them more difficult to finance due to perceived risk. Some cross-cutting problems in financing circular business models can increase counterparty risks due to more parties, reporting and transaction costs. Taken together the accounting rules, relative illiquidity of green finance markets, financing risks and other market structure issues, capital flow to sustainable causes is likely reduced. The solution to capital adequacy ratio problem may also present a solution in how to move circlar economy and hence would be desirable to financial institutions. This could also mean initial action is well known and doable while [transition risks](https://www.caixabankresearch.com/en/climate-change-green-transition-and-financial-sector) (see the image for clarification) can be still handled.

The change needs to be coordinated in a globally connected world when most of the enterprise participating in the economy are small and medium (SME) sized. For example, according to Eurostat [Statistics on small and medium-sized enterprises](https://ec.europa.eu/eurostat/statistics-explained/index.php/Statistics_on_small_and_medium-sized_enterprises) 99% are such enterprises in Europe. From a systemic, financial supply-chain perspective, larger companies pushing increasing reporting obligations further in the supply-chain thus increasing costs without appropriate financing or increased cash-flow is a difficult issue. So it would be important to enhance the ability to report and reduce transaction costs so that the opportunity costs for banks would favor more circular or sustainable credit lines instead of "standard SME finance" or mortgage or retail banking. This would likely enhance sustainability project appraisal and equity investment capability.

An in depth discussion of global financial system problems and how to innovate as part of supply-chains are not in the scope of this introduction. These could be very well spefic business innovations.

### 1.1 Problem Statement

For the purpose of the problem context in this specification [Accelerating the transition to the circular economy: Improving access to finance for circular economy projects](https://op.europa.eu/en/publication-detail/-/publication/21a71687-ee30-11e9-a32c-01aa75ed71a1) poster is used to introduce a succinct set of point, while also noting the [the report the poster](https://op.europa.eu/en/publication-detail/-/publication/02590134-4548-11e9-a8ed-01aa75ed71a1) is based on.

1. Lack of a level playing field for circular economy businesses.
2. Insufficient value-chain collaboration.
3. Lack of product longevity in business models.
4. Insufficient market participation by consumers.
5. Lack of integration of the costs of externalities.
6. Lack of financial knowledge about the circular economy.
7. Insufficient action by first movers.

Recommendations to the financial sector

1. Develop definitions, taxonomy and tools to measure an activity’s circularity.
2. Analyse the risk of a linear economy and adjust credit risks assessment methods accordingly.
3. Increase the financial sector’s awareness and knowledge of the circular economy.
4. Label financial instruments fit for circular economy projects.
5. Establish risk-sharing financial instruments and create a pool of experts.

Recommendations to project promoters

1. Identify circular sources of revenues in an organisation and update its strategy.
2. Disclose environmental and social benefits through credible, standardised methods.
3. Take part in collaborative communities of practice to identify opportunities and business partnerships.
4. Increase the capacity of organisations to conceive and implement circular economy projects through training staff.

Recommendations to policy makers

1. Ensure that linear risks are sufficiently evaluated and disclosed.
2. Develop definitions, taxonomy, and benchmarks to measure environmental performance.
3. Establish technical and financial advisory services to support the development of business models.
4. Create favourable framework conditions for circular economy projects through policy actions.
5. Make public authorities act as facilitators for the circular economy.
6. Prioritise financing circular economy investments and businesses through EU financial instruments.

The poster refers further to [The European Investment Bank Circular Economy Guide](https://www.eib.org/en/publications/the-eib-in-the-circular-economy-guide) and [High-Level Expert Group on sustainable finance](https://ec.europa.eu/info/publications/180131-sustainable-finance-report_en).

### 1.2 Proposal

We propose to decentralized identifier and verifiable credentials to uniquely identify data that can be used in environmental, social and governance (ESG) reporting, impact analysis, and sustainable finance (e.g. securitization, structured finance, impact finance) when business specific tooling has been built. The purpose is to establish an audited trail of data and its reporting that can be referenced by multiple parties, a common source of truth. Explicitly noted:

1. The core data structure should be an envelope that gives an identifier for this kind of a ESG, "impact evidence" or financially relevant data hoisted from industry specific, semantic data. This way the financial system can have the data it needs to operate while acting as a conduit for the other supply-chain data. That is, supply-chains are roughly financial, documentation and physical (logistics) that usually are somewhat joined in ERP or CRM systems. This way financial data could be more readily linked to operational data while also supporting supply-chain actions. Specifically this is helpful for [GHG Protocol](http://ghgprotocol.org/) type reporting where corporate value chain emissions are gathered and reported.
2. The protocol should be simple and broadly applicable. It should allow extensions for certain industry specific uses cases as it allows for industry specific data.
3. Implicitly the financial data should be neutral so that it is just held by one or more parties and signed by other parties for stated purposes. So the system use "law as a platform", broadly being compatible with [contracts](https://en.wikipedia.org/wiki/Contract) as understood broadly by [common law systems](https://en.wikipedia.org/wiki/Legal_origins_theory) specifically with respect to documents when they are signed.
4. Base data collection and curation is not free to individuals or organizations and should be rewarded. This is relevant to certain types of nature-based or green-grey projects for instance.
5. Data and knowledge intensive products from the data by researchers or engineering companies to new or riskier projects are not free to produce. This may be the case especially on nature-based on green projects. While applications may be local, the knowledge and products may have global markets. Generating such knowledge likely requires work and taking risks so should be rewarded if used broadly.
6. The framework should allow "green tagging" innovations so innovations in later stages could be "unpermissioned" but reward the source side of supply-chain. So it should allow IPR and revenue sharing to encourage new circular business models that are not so intimiately confined on some certain supply-chains and current business models enterprises are part of. Otherwise it will be difficult circularize or re-capitalize the circular cycles with new innovations.
7. There is considerable uncertainty amongst financing and urban planning community on what works and why and plain "comic book explanations" of natural, regenerative processes could help to bring clarity. So this sort of education or "story telling" community could be important factor in making the transition.
8. Many charities and NGOs also collect data and do reports. In some cases this is a significant burden for local authorities or governments. This may mean there are markets for "transoformation products" that create more readily accepted formats out of this.
9. There already exists publicly available environmental data (PAED) that should be included either as linked or otherwise.
10. Since the system is distributed, it should be possible to check if two documents contain the same data.

The issuance and operation of the data hubs and actors should be open-ended so that it does not require permission to join. Reduced transaction costs and availability of data should in turn drive coordination capabilities for economic entities and facilitate innovations and software on multiple levels so everyone has an incentive to work together.

The following sections explain key issues in more detail.

## 2. Data governance

The purpose of this data framework is to support transition to circular economy and deepen it using financial system. The participants in the data framework can be at least in the following roles:

1. **Operators:** Entity operating the data hub and agents in the network also on behalf of users or proxying access to authenticated data in user systems.
2. **Users:** Entities accessing the data hub and agents in the network. These can be any entities but notably financial institutions, enterprises, public authorities, non-governmental organizations and individual users.

The operators can be enterprises, trusts or other parties that are legally allowed to handle the data and the the other participants trust. The core principle of Circomy data framework is adversarial interoperability as defined by [Electronic Frontier Foundation: Adversarial Interoperability](https://www.eff.org/deeplinks/2019/10/adversarial-interoperability)
> competitive, innovative, dynamic marketplace, you need adversarial interoperability: that’s when you create a new product or service that plugs into the existing ones without the permission of the companies that make them.  Think of third-party printer ink, alternative app stores, or independent repair shops that use compatible parts from rival manufacturers to fix your car or your phone or your tractor.

Permissionless access to the data network means that the framework can grow without undue business or legal costs or risks or coordinated anti-competitive practices by other participants in the network. This access also requires special attention on legal frameworks such GDPR, appropriate encryption and electronic signing (e.g. [eIDAS](https://ec.europa.eu/digital-single-market/en/trust-services-and-eid)) technologies.

Many of these issues are currently being discussed. Notable are:

- [EU Digital Single Market Guidance on private sector data sharing](https://ec.europa.eu/digital-single-market/en/guidance-private-sector-data-sharing),
- [Building Trust Through Data Foundations: A Call for a Data Governance Model to Support Trustworthy Data Sharing](https://www.southampton.ac.uk/wsi/enterprise-and-impact/white-papers.page) by **Sophie Stalla-Bourdillon**, **Alexsis Wintour** and **Laura Carmichael** and
- [Web of Trust: Encrypted Data Vaults](https://github.com/WebOfTrustInfo/rwot9-prague/blob/master/final-documents/encrypted-data-vaults.md) by **Amy Guy**, **David Lamers**, **Tobias Looker**, **Manu Sporny** and **Dmitri Zagidulin**.

The following are the main relevant points quoted from Building Trust Through Data Foundastions:

**1. A comprehensive rulebook**

A data governance model must have a comprehensive rulebook for the usage, sharing, and re-usage of personal and non-personal data, including a robust ethical framework, which should be made publicly available. This rulebook should:

- Go beyond privacy and data protection compliance and set forth both substantial and process-related safeguards for the whole lifecycle of the data to be shared and (re-)used, that considers the entire data spectrum.
- Clearly state the objectives of the data sharing and (re-)usage activities to be conducted by the participants, identify key roles and set workflows and safeguards for decision-making relating to data usage, sharing, and re-usage.
- Be made publicly available for obvious reasons of transparency and accountability.

**2. An independent governance body**

A data governance model must have a strong, independent governance body comprised of independent data stewards with interdisciplinary expertise. The data steward role should be at the core of any data governance model and oversee the decision-making body. This independent governance body should:

- Help to set up data-sharing arrangements and workflows between key actors.
- Inform decision-making related to data usage, sharing, and re-usage, and systematically monitor data sharing and data usage practices.
- Be involved in risk assessment and effective threat modelling. In high risk situations, independent data stewards should be given a whistle-blower role.
- Commission external roles where appropriate and the necessary authorisation is in place, such as external auditors, to complement their assessment.

**3. An inclusive decision-making body**

A data governance model must have a decision-making body that engages participants (in particular data providers) and represents the interests of data subjects. This inclusive decision-making body should:

- Implement standardised processes that provide meaningful representation of data subjects’ interests.
- Involve data providers in such processes so that they are kept in the loop and adapt their practices over time.

**4. A standardised process for flexible membership**

A data governance model must have a standardised process to enable relative flexibility in its membership so that:

- The structure can smoothly grow overtime without exaggerated (legal) costs.
- The risks of harm arising through anti-competitive practices are mitigated, e.g. organisations are not excluded from joining a data governance model without reasonable justification.41

**5. A trust-enhancing technical and organisational infrastructure**

It is crucial to distinguish between the sharing of data, which should happen through a trust-enhancing technical and organisational infrastructure, and the creation of the legal structure (e.g. through contracts, or the incorporation of a new legal entity). The creation of the legal structure should not automatically lead to data sharing. Data flows should only be triggered once the particularities of each use case are known. Importantly, there is no fundamental opposition between what some have called “the technological model”42 and the legal model for data sharing.
On the contrary, we suggest that the building of the data governance model, including the selection and refinement of the legal structure, should be informed by current data sharing technological capabilities.
A data governance model must therefore rely upon a trust-enhancing technical and organisational infrastructure, which should:

- Be able to reduce unnecessary data movements.
- Tailor the amount of data to specific and legitimate purposes and action the sharing once these purposes have been identified.
- Monitor queries.
- Ensure confidentiality through e.g. role-based and purpose-based access control, de-identification solutions including noise injection, multiplication of layers (through federated learning or the “student-teacher” approach), and/or secure multi-party computation depending upon use case.
- Ensure a high level of accountability through e.g. decentralised solutions such as distributed ledgers or more simply standardised access to data.
- Provide a level of data security that is adapted to both the sensitivity of the data, and the purpose(s) for its usage, sharing, and re-usage.

**6. A well-regulated legal structure**

A data governance model must have a well-regulated legal structure, which should:

- Represent all stakeholders in decision-making processes, e.g. to give data providers – from start-ups to multinational companies – and data subjects rights and opportunities to voice their opinions regardless of their nature, size, or number.
- Provide effective authoritative oversight.
- Have a mature compliance and enforcement function.
- Be able to manage and examine escalated complaints with recourse to the Courts if required

## 3. Guiding cases

A conclusion of the main enabling technological points and some high level target cases.

### 3.1 Reporting

Regulations such as EU Sustainable Finance taxonomy and investor demand for green assets create a need for verifiable reporting efficiently. In this context especially environment, social and governance (ESG) reporting is central and several proprietary methods are already in use. It should be notable the underlying data is approxiately the same, the methods to extract further insight or ways to present the data may wary.

Plenty of data has been collected and is currently collected but it may not be directly useablein various reporting purposes without further transformation. While there are currently attempts to unify methods and reporting, it takes time and already and will be collected data needs to be transformed. In many cases data collection is also an expensive and laborious process that should be appropriately rewarded.

Reporting is not a good proxy for technological, environmental or climate risks as it is backwards looking.

### 3.2 Impact evaluation

Impact evaluation is profession a set of methodologies to assess the effect of actions taken. Impact evaluation and using the results and learnings are particularly important to accelerate the pace and quantity of sustainable and impact finance.

To do more than reporting and help moving into circular and sustainable economy and building resilience and adaptting systems, to facilitate brown transition finance and green finance, the framework needs to support methodology to do so. This means in relevant parts the saved documents need to define an expectation for monitoring and drawing scientifically valid conclusions. The standards used to support the data need to support CREAM definition, to be **C**clear, **R**elevant, **E**conomic, **A**dequate and **M**onitorable. Other known acronym for the same purpose is SMART. These documents can be linked to financial objectives and used as a tool to transfer and adapt learning to improve and accelerate adaptation and other project development globally.

### 3.3 Material and energy flows

Material flows, and associated energy flows, are an important part of circular economy especially due to urbanization. For example [Sitra](https://www.sitra.fi/en/) notes in its [material economics](https://www.sitra.fi/en/publications/circular-economy-powerful-force-climate-mitigation/) publication

> circular economy can make deep cuts to emissions from heavy industry: in an ambitious scenario, as much as 296 million tons CO2 per year in the EU by 2050, out of 530 Mt in total – and some 3.6 billion tonnes per year globally. Making better use of the materials that already exist in the economy thus can take EU industry halfway towards net-zero emissions. Moreover, doing so often is economically attractive.

It is notable that the markets for recycled construction and demolition waste do not function well currently. This is the case for water and nutrients flows and even electronics which seem to have some similarities. Rather than try to create "recycling markets" one-by-one, one could create information on in-stock materials (e.g. buildings) and their qualities to make the materials visible and create a price signal. In effect create [certificated stock](https://www.investopedia.com/terms/c/certificatedstock.asp) (example: [Cotton Deliverer's & Receiver's Guide](https://www.theice.com/publicdocs/futures_us_reports/cotton/Cotton_Deliverers_Guide.pdf)) bring them to a merchant trading. This would allow the same financing options as virgin materials and one could assume recycled materials would be competive against virgin materials especially when accounting for life-cycle costs. The materials likely need processing such as concrete on pH or metals to remove impurities, but having more information on in-stock quantities, timeliness and market demand would also allow investing to refineries, logistics and might introduce demolition and construction innovations throughout the supply-chain if they were financially beneficial.

Some of the issues are discussed also in [Accelerating the transition to the circular economy: Improving access to finance for circular economy projects](https://op.europa.eu/en/publication-detail/-/publication/21a71687-ee30-11e9-a32c-01aa75ed71a1).

#### 3.4 Investing and securitization (and transparency)

Circular economy seem to have more complex counterparty risks (more parties) and more complex operational expenses. It looks like almost essential to improve reporting accuracy, timeleness, trustworthiness and data availability across company boundaries. This should be beneficial even in current linear economy even if not explicitly considering green or circular economoy. With improved impact evaluation process likely more projects will be financed and results and learning transferred to new projects. Reduced transaction costs and improvements in reporting may allow for various impact financing cases to be developed and even business models that are dependent more on dynamic pricing or more complex financing arrangements.

It would be benficial if the collected data could at some point support securitization and due diligence operations. Reducing transaction costs and increasing transparency should increase liqudity of green assets and their overall desirability. An interesting target case would be to support "circular transparency" through the whole financial chain to derivatives markets. [How to save the world: 1 measure it](https://www.euromoneyconferences.com/article/3771142/how-to-save-the-world-1-measure-it.)

Moreover, increased supply of green investment assets combined with adding tokenized securitization should bring other benefits. Such as reduced liquidity and market risk, and financing and opportunity costs. Easier to buy and sell financial assets within a desired time since there are more counterparties at the markets reducing transaction and search costs, financing and opportunity costs. These are likely appealing factors in finance and executed correctly should increase capital flows to sustainable causes.
