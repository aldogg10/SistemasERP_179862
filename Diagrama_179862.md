flowchart LR
    customer((Customer))
    lead((Lead))
    supplier((Supplier))
    activities((Activities))
    bpm((Business Partner Master))

    opportunity((Opportunity))
    pricing((Pricing))
    salesQuotation((Sales Quotation))
    salesOrder((Sales Order))
    deliveryNote((Delivery Note))
    arInvoice((AR Invoice))
    incomingPayments((Incoming Payments))
    outgoingPayments((Outgoing Payments))
    cashManagement((Cash Management))
    apAr((AP / AR))

    cec((Customer Equipment Card))
    serviceCall((Service Call))
    serviceContract((Service Contract))
    serviceBilling((Service Billing))

    itemMaster((Item Master))
    warehouseMgmt((Warehouse Management))

    purchaseRequest((Purchase Request))
    purchaseQuotation((Purchase Quotation))
    purchaseOrder((Purchase Order))
    goodsReceiptPO((Goods Receipt PO))
    apInvoice((AP Invoice))

    demandPlanning((Demand Planning))
    billOfMaterials((Bill of Materials))
    mrp((Material Requirements Planning))
    sourcing((Sourcing))
    productionOrder((Production Order))
    issueToProduction((Issue to Production))
    receiptFromProduction((Receipt from Production))

    journalEntries((Journal Entries))
    inventoryAuditReport((Inventory Audit Report))
    backorderReporting((Backorder Reporting))
    accountBalancesReport((Account Balances Report))
    productReporting((Product Reporting))
    financialReporting((Financial Reporting))
    reconciliation((Reconciliation))

    chartOfAccounts((Chart of Accounts))
    generalLedger((General Ledger Accounts))
    glDetermination((G/L Account Determination))
    costAccounting((Cost Accounting))

    customer --- activities
    customer --- lead
    customer --- cec
    customer --- opportunity
    lead --- supplier
    lead --- opportunity
    supplier --- purchaseQuotation
    supplier --- bpm

    opportunity --- pricing
    pricing --- salesQuotation
    salesQuotation --- salesOrder
    salesOrder --- deliveryNote
    deliveryNote --- arInvoice
    arInvoice --- incomingPayments
    incomingPayments --- outgoingPayments

    cec --- itemMaster
    cec --- serviceCall
    serviceCall --- serviceContract
    serviceContract --- serviceBilling
    serviceBilling --- arInvoice

    purchaseRequest --- purchaseQuotation
    purchaseQuotation --- purchaseOrder
    purchaseOrder --- salesOrder
    purchaseOrder --- goodsReceiptPO
    goodsReceiptPO --- deliveryNote
    goodsReceiptPO --- issueToProduction
    goodsReceiptPO --- apInvoice
    apInvoice --- arInvoice
    apInvoice --- outgoingPayments
    apInvoice --- apAr

    itemMaster --- pricing
    itemMaster --- warehouseMgmt
    warehouseMgmt --- salesOrder
    warehouseMgmt --- demandPlanning
    demandPlanning --- productionOrder
    demandPlanning --- backorderReporting

    billOfMaterials --- mrp
    billOfMaterials --- demandPlanning
    mrp --- sourcing
    sourcing --- productionOrder
    productionOrder --- purchaseOrder
    productionOrder --- issueToProduction
    productionOrder --- backorderReporting
    issueToProduction --- receiptFromProduction
    issueToProduction --- inventoryAuditReport
    receiptFromProduction --- accountBalancesReport
    receiptFromProduction --- productReporting

    inventoryAuditReport --- backorderReporting
    inventoryAuditReport --- accountBalancesReport
    accountBalancesReport --- productReporting
    productReporting --- financialReporting
    financialReporting --- reconciliation

    chartOfAccounts --- generalLedger
    generalLedger --- glDetermination
    glDetermination --- costAccounting
    costAccounting --- journalEntries
    journalEntries --- receiptFromProduction
    apAr --- arInvoice
    apAr --- cashManagement
    cashManagement --- incomingPayments
    cashManagement --- reconciliation

    linkStyle 0,1,2,3,4,5,6,7 stroke:#2ca02c,stroke-width:2px
    linkStyle 8,9,10,11,12,13,14 stroke:#ff7f0e,stroke-width:2px
    linkStyle 15,16,17,18,19 stroke:#ffcc00,stroke-width:2px
    linkStyle 20,21,22,23,24,25,26,27,28,29 stroke:#1f77b4,stroke-width:2px
    linkStyle 30,31,32,33,34,35 stroke:#7f7f7f,stroke-width:2px
    linkStyle 36,37,38,39,40,41,42,43,44,45,46 stroke:#5e2ca5,stroke-width:2px
    linkStyle 47,48,49,50,51 stroke:#e377c2,stroke-width:2px
    linkStyle 52,53,54,55,56,57,58,59,60 stroke:#d62728,stroke-width:2px
