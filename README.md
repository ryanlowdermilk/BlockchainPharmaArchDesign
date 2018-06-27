Pharma Sample for Azure Blockchain Workbench
====================================================

Overview 
---------
This is a sample of a possible Blockchain deployment for Pharma. It invovles multiple Actors/Application Roles e.g. Pharma Manufacturer, Whole Saler, Distribution, Pharamacy, End User.

Application Roles 
------------------

| Name         | Description                                                                                         |
|--------------|-----------------------------------------------------------------------------------------------------|
| Manufacturer | A company involved in the creation and selling of pharmaceuticals                                   |
| Wholesaler   | A company invovled in the purchase and resale of pharmaceuticals.                                   |
| Distributor  | A company invovled in the distribution of pharmaceuticals.                                          |
| Customer     | A pharamacy who has placed the medication order.                                                    |

States 
-------

| Name                 | Description                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------|
| Active               | Indicates that an asset is available for being bought.                                                      |
| Offer Placed         | Indicates a buyer's intention to buy.                                                                       |
| Pending Inspection   | Indicates a buyer's request to the Inspector to inspect the asset under consideration.                      |
| Inspected            | Indicates the Inspector's approval to buy the asset under consideration.                                    |
| Appraised            | Indicates the Appraiser's approval to buy the asset under consideration.                                    |
| Notional Acceptance  | Indicates that both the Inspector and the Appraiser have approved buying the asset under consideration.     |
| Seller Accepted      | Indicates the owner's approval to accept the offer made by the buyer.                                       |
| Buyer Accepted       | Indicates the buyer's approval for the owner's approval.                                                    |
| Accepted             | Indicates that both the buyer and the seller have agreed to the transfer of the asset under consideration.  |
| Terminated           | Indicates owner's disapproval to continue with selling the asset under consideration.                       |

Workflow Details
----------------

![](media/1a14a6336d8a8b1adfe5c3689ab954b2.png)

The following state transition diagram articulates the possible flows, and the
various transition functions at each state. Each user is only allowed to take
certain actions depending on the application role. Instance roles indicate that
only the user with the application role assigned to the specific contract is
able to take actions on the contract. 

The happy path highlighted shows in a given asset transfer contract, an instance
owner can place an asset up for sale, and a potential buyer can place an
offer. The two parties can negotiate and once an offer amount is agreed upon, an
inspector and an appraiser working for the instance buyer will
participate. After their involvement, the buyer and the owner can choose to move
forward and ultimately complete the transaction. 

 
