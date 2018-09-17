
 ## How to contribute
Share your knowledge with the community by contributing to Cedrus One!
If you would like to become a contributor, please send an email to cedrusone@cedruslogistics.com with the subject “Contribute”.

 ## Contributors
- [IKE INDA](https://www.linkedin.com/in/ikeinda/)
 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html>
  <head>
    <META http-equiv="Content-Type" content="text/html; charset=utf-8">
  </head>
  <body>
    <div style="text-align: center">
<p align="center">
  <img alt="CedrusONE" src="https://github.com/cedruslogistics/CedrusONE/blob/master/docs/design/logo/Cedrus%20ONE%20logo-04.png" width="200"/>
</p>
      </div>
    <h1>
                Database Schema
                </h1>
    <div id="toc">
      <ul>
        <li><b>Account</b><ul>
            <li class="table"><a href="#1431676148">Account</a></li>
            <li class="table"><a href="#1390627997">AccountType</a></li>
            <li class="table"><a href="#1662628966">BankStatement</a></li>
            <li class="table"><a href="#1710629137">BankStatementLine</a></li>
            <li class="table"><a href="#1947153982">BillingAccount</a></li>
            <li class="table"><a href="#1221579390">CreditCard</a></li>
            <li class="table"><a href="#34099162">PaymentTermLine</a></li>
            <li class="table"><a href="#123147484">PaymentType</a></li>
          </ul>
        </li>
        <li><b>Accounting</b><ul>
            <li class="table"><a href="#1102626971">Bill</a></li>
            <li class="table"><a href="#1150627142">BillDetail</a></li>
            <li class="table"><a href="#471672728">Charge</a></li>
            <li class="table"><a href="#519672899">Currency</a></li>
            <li class="table"><a href="#567673070">CurrencyRate</a></li>
            <li class="table"><a href="#759673754">Deposit</a></li>
            <li class="table"><a href="#1623676832">DiscountItem</a></li>
            <li class="table"><a href="#1719677174">GiftCertificate</a></li>
            <li class="table"><a href="#347148282">Invoice</a></li>
            <li class="table"><a href="#1797581442">InvoiceLine</a></li>
            <li class="table"><a href="#1941581955">InvoicePayment</a></li>
            <li class="table"><a href="#1893581784">InvoiceRefund</a></li>
            <li class="table"><a href="#2091154495">Payment</a></li>
            <li class="table"><a href="#1995154153">PaymentMethod</a></li>
            <li class="table"><a href="#1989582126">PaymentTerm</a></li>
            <li class="table"><a href="#711673583">RecurringPayment</a></li>
            <li class="table"><a href="#82099333">Tax</a></li>
            <li class="table"><a href="#2002106173">TaxCategory</a></li>
          </ul>
        </li>
        <li><b>Address</b><ul>
            <li class="table"><a href="#484196775">Address</a></li>
            <li class="table"><a href="#1509580416">AddressType</a></li>
            <li class="table"><a href="#1323151759">Country</a></li>
            <li class="table"><a href="#1355151873">StateProvince</a></li>
          </ul>
        </li>
        <li><b>Company</b><ul>
            <li class="table"><a href="#1156199169">Company</a></li>
            <li class="table"><a href="#1108198998">Contact</a></li>
            <li class="table"><a href="#807673925">Department</a></li>
            <li class="table"><a href="#2055678371">Division</a></li>
            <li class="table"><a href="#178099675">Employee</a></li>
            <li class="table"><a href="#226099846">EmployeeCategory</a></li>
            <li class="table"><a href="#478624748">EmployeeRole</a></li>
            <li class="table"><a href="#1198627313">Note</a></li>
            <li class="table"><a href="#430624577">Role</a></li>
            <li class="table"><a href="#4195065">Setting</a></li>
          </ul>
        </li>
        <li><b>dbo</b><ul>
            <li class="table"><a href="#1300199682">InventoryMethod</a></li>
          </ul>
        </li>
        <li><b>Inventory</b><ul>
            <li class="table"><a href="#1934629935">Adjustment</a></li>
            <li class="table"><a href="#2030630277">AdjustmentLine</a></li>
            <li class="table"><a href="#946102411">Incoterms</a></li>
            <li class="table"><a href="#898102240">Inventory</a></li>
            <li class="table"><a href="#994102582">InventoryLine</a></li>
            <li class="table"><a href="#619149251">Item</a></li>
            <li class="table"><a href="#1911677858">ItemType</a></li>
            <li class="table"><a href="#574625090">StockQuantityHistory</a></li>
            <li class="table"><a href="#1767677345">TransferOrder</a></li>
          </ul>
        </li>
        <li><b>Log</b><ul>
            <li class="table"><a href="#334624235">ActivityLog</a></li>
            <li class="table"><a href="#382624406">ActivityLogType</a></li>
            <li class="table"><a href="#628197288">InventoryLog</a></li>
            <li class="table"><a href="#526624919">TransactionLog</a></li>
          </ul>
        </li>
        <li><b>Manufacturing</b><ul>
            <li class="table"><a href="#1204199340">Assembly</a></li>
            <li class="table"><a href="#1252199511">AssemblyDetail</a></li>
            <li class="table"><a href="#964198485">Bom</a></li>
            <li class="table"><a href="#836198029">BomItem</a></li>
            <li class="table"><a href="#884198200">BomItemType</a></li>
          </ul>
        </li>
        <li><b>Person</b><ul>
            <li class="table"><a href="#1396200024">Person</a></li>
          </ul>
        </li>
        <li><b>Pointofsale</b><ul>
            <li class="table"><a href="#466100701">PosConfiguration</a></li>
            <li class="table"><a href="#418100530">PosDiscount</a></li>
            <li class="table"><a href="#370100359">PosOrder</a></li>
            <li class="table"><a href="#322100188">PosOrderLine</a></li>
          </ul>
        </li>
        <li><b>Product</b><ul>
            <li class="table"><a href="#802101898">Attribute</a></li>
            <li class="table"><a href="#850102069">AttributeLine</a></li>
            <li class="table"><a href="#610101214">Category</a></li>
            <li class="table"><a href="#658101385">Image</a></li>
            <li class="table"><a href="#1527676490">KitItem</a></li>
            <li class="table"><a href="#388196433">KitItemType</a></li>
            <li class="table"><a href="#1858105660">Manufacturer</a></li>
            <li class="table"><a href="#238623893">MeasureDimension</a></li>
            <li class="table"><a href="#286624064">MeasureWeight</a></li>
            <li class="table"><a href="#1006626629">Package</a></li>
            <li class="table"><a href="#1060198827">PricingRule</a></li>
            <li class="table"><a href="#27147142">Product</a></li>
            <li class="table"><a href="#1403152044">ProductAttribute</a></li>
            <li class="table"><a href="#651149365">ProductImage</a></li>
            <li class="table"><a href="#1810105489">ProductReview</a></li>
            <li class="table"><a href="#754101727">ProductTaxes</a></li>
            <li class="table"><a href="#1483152329">RelatedProduct</a></li>
            <li class="table"><a href="#706101556">Template</a></li>
            <li class="table"><a href="#859150106">Vehicle</a></li>
            <li class="table"><a href="#939150391">VehicleDefinition</a></li>
          </ul>
        </li>
        <li><b>Purchasing</b><ul>
            <li class="table"><a href="#327672215">PurchaseOrder</a></li>
            <li class="table"><a href="#539148966">PurchaseOrderDetail</a></li>
            <li class="table"><a href="#763149764">Vendor</a></li>
          </ul>
        </li>
        <li><b>Reporting</b><ul>
            <li class="table"><a href="#1671677003">ExpenseReport</a></li>
          </ul>
        </li>
        <li><b>Sales</b><ul>
            <li class="table"><a href="#683149479">Customer</a></li>
            <li class="table"><a href="#52195236">ProductService</a></li>
            <li class="table"><a href="#1714105147">Quotation</a></li>
            <li class="table"><a href="#1762105318">QuotationDetail</a></li>
            <li class="table"><a href="#75147313">SalesOrder</a></li>
            <li class="table"><a href="#2126630619">SalesOrderDetail</a></li>
            <li class="table"><a href="#1173579219">SalesPerson</a></li>
            <li class="table"><a href="#1125579048">SalesTaxRate</a></li>
            <li class="table"><a href="#1077578877">SpecialOffer</a></li>
          </ul>
        </li>
        <li><b>Shipping</b><ul>
            <li class="table"><a href="#340196262">Airline</a></li>
            <li class="table"><a href="#1131151075">Booking</a></li>
            <li class="table"><a href="#1275151588">BookingDetail</a></li>
            <li class="table"><a href="#676197459">Carrier</a></li>
            <li class="table"><a href="#772197801">CarrierService</a></li>
            <li class="table"><a href="#2103678542">Port</a></li>
            <li class="table"><a href="#2050106344">Return</a></li>
            <li class="table"><a href="#2098106515">ReturnRequest</a></li>
            <li class="table"><a href="#94623380">ReturnRequestAction</a></li>
            <li class="table"><a href="#46623209">ReturnRequestReason</a></li>
            <li class="table"><a href="#1035150733">Route</a></li>
            <li class="table"><a href="#1522104463">Shipment</a></li>
            <li class="table"><a href="#1570104634">ShipmentDetail</a></li>
            <li class="table"><a href="#148195578">ShippingLine</a></li>
            <li class="table"><a href="#190623722">ShippingMethod</a></li>
            <li class="table"><a href="#142623551">ShippingMethodRestrictions</a></li>
            <li class="table"><a href="#1435152158">ShippingRate</a></li>
            <li class="table"><a href="#532196946">ShippingTerms</a></li>
            <li class="table"><a href="#987150562">Trip</a></li>
          </ul>
        </li>
        <li><b>System</b><ul>
            <li class="table"><a href="#292196091">Backup</a></li>
            <li class="table"><a href="#1806629479">Cache</a></li>
            <li class="table"><a href="#622625261">Configuration</a></li>
            <li class="table"><a href="#718625603">ConfigurationDetail</a></li>
            <li class="table"><a href="#814625945">Event</a></li>
            <li class="table"><a href="#862626116">EventType</a></li>
            <li class="table"><a href="#766625774">Installer</a></li>
            <li class="table"><a href="#670625432">Language</a></li>
            <li class="table"><a href="#1294627655">Maintenance</a></li>
            <li class="table"><a href="#1342627826">Preferences</a></li>
            <li class="table"><a href="#1348199853">UserReminder</a></li>
          </ul>
        </li>
        <li><b>Transactions</b><ul>
            <li class="table"><a href="#1479676319">CashRefund</a></li>
            <li class="table"><a href="#279672044">Check</a></li>
            <li class="table"><a href="#1618104805">CreditMemo</a></li>
            <li class="table"><a href="#855674096">Job</a></li>
            <li class="table"><a href="#903674267">JobType</a></li>
            <li class="table"><a href="#951674438">JournalEntry</a></li>
            <li class="table"><a href="#1335675806">Task</a></li>
          </ul>
        </li>
        <li><b>Warehousing</b><ul>
            <li class="table"><a href="#1186103266">Location</a></li>
            <li class="table"><a href="#1234103437">LocationRoute</a></li>
            <li class="table"><a href="#436196604">LocationType</a></li>
            <li class="table"><a href="#1282103608">Move</a></li>
            <li class="table"><a href="#1330103779">MoveLine</a></li>
            <li class="table"><a href="#1090102924">Picking</a></li>
            <li class="table"><a href="#1138103095">PickingType</a></li>
            <li class="table"><a href="#1083150904">PickupOrder</a></li>
            <li class="table"><a href="#1227151417">PickupOrderDetail</a></li>
            <li class="table"><a href="#910626287">Receipt</a></li>
            <li class="table"><a href="#958626458">ReceiptDetail</a></li>
            <li class="table"><a href="#2007678200">Release</a></li>
            <li class="table"><a href="#1042102753">Warehouse</a></li>
          </ul>
        </li>
      </ul>
    </div>
    <div class="table">
      <h2 id="1431676148"><a href="#toc" class="tocref">⇧</a>Table Account.Account</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Account"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Account"></span>AccountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Number</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Desciption</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Active</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AccountTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ParentId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1390627997"><a href="#toc" class="tocref">⇧</a>Table Account.AccountType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_AccountType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_AccountType"></span>AccountTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1662628966"><a href="#toc" class="tocref">⇧</a>Table Account.BankStatement</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_BankStatement"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_BankStatement"></span>BankStatementId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Reference</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Date</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>StartBalance</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>EndBlance</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1710629137"><a href="#toc" class="tocref">⇧</a>Table Account.BankStatementLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_BankStatementLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_BankStatementLine"></span>BankStatementLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Date</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Reference</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Sequence</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>StatementId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>BankAccountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AccountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1947153982"><a href="#toc" class="tocref">⇧</a>Table Account.BillingAccount</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_BillingAccount"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_BillingAccount"></span>BillingAccountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Memo</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>NextBillCycleDate</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LastBillDate</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LastBillCycleDate</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Frequency</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>Annually, Daily, Hourly, Monthly, Weekly</td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CustomerId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1221579390"><a href="#toc" class="tocref">⇧</a>Table Account.CreditCard</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CreditCard"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CreditCard"></span>CreditCardId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="34099162"><a href="#toc" class="tocref">⇧</a>Table Account.PaymentTermLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentTermLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentTermLine"></span>PaymentTermLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="123147484"><a href="#toc" class="tocref">⇧</a>Table Account.PaymentType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentType"></span>PaymentTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1102626971"><a href="#toc" class="tocref">⇧</a>Table Accounting.Bill</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Bill"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Bill"></span>BillId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1150627142"><a href="#toc" class="tocref">⇧</a>Table Accounting.BillDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_BillDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_BillDetail"></span>BillDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="471672728"><a href="#toc" class="tocref">⇧</a>Table Accounting.Charge</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Charge"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Charge"></span>ChargeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>BillingAccountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="519672899"><a href="#toc" class="tocref">⇧</a>Table Accounting.Currency</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Currency"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Currency"></span>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Symbol</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="567673070"><a href="#toc" class="tocref">⇧</a>Table Accounting.CurrencyRate</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CurrencyRate"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CurrencyRate"></span>CurrencyRateId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>EffectiveDate</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ExchangeRate</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="759673754"><a href="#toc" class="tocref">⇧</a>Table Accounting.Deposit</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Deposit"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Deposit"></span>DepositId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>ExchangeRate</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Memo</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Date</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AccountId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1623676832"><a href="#toc" class="tocref">⇧</a>Table Accounting.DiscountItem</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_DiscountItem"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_DiscountItem"></span>DiscountItemId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1719677174"><a href="#toc" class="tocref">⇧</a>Table Accounting.GiftCertificate</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_GiftCertificate"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_GiftCertificate"></span>GiftCertificateId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="347148282"><a href="#toc" class="tocref">⇧</a>Table Accounting.Invoice</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Invoice"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Invoice"></span>InvoiceId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CustomerId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1797581442"><a href="#toc" class="tocref">⇧</a>Table Accounting.InvoiceLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_InvoiceLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_InvoiceLine"></span>InvoiceLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1941581955"><a href="#toc" class="tocref">⇧</a>Table Accounting.InvoicePayment</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th></th>
            <th>InvoiceId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>PaymentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1893581784"><a href="#toc" class="tocref">⇧</a>Table Accounting.InvoiceRefund</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_InvoiceRefund"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_InvoiceRefund"></span>InvoiceRefundId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2091154495"><a href="#toc" class="tocref">⇧</a>Table Accounting.Payment</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Payment"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Payment"></span>PaymentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>PaymentTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>PaymentMethodId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1995154153"><a href="#toc" class="tocref">⇧</a>Table Accounting.PaymentMethod</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentMethod"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentMethod"></span>PaymentMethodId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1989582126"><a href="#toc" class="tocref">⇧</a>Table Accounting.PaymentTerm</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentTerm"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PaymentTerm"></span>PaymentTermId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="711673583"><a href="#toc" class="tocref">⇧</a>Table Accounting.RecurringPayment</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_RecurringPayment"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_RecurringPayment"></span>RecurringPaymentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="82099333"><a href="#toc" class="tocref">⇧</a>Table Accounting.Tax</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Tax"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Tax"></span>TaxId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2002106173"><a href="#toc" class="tocref">⇧</a>Table Accounting.TaxCategory</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_TaxCategory"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_TaxCategory"></span>TaxCategoryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="484196775"><a href="#toc" class="tocref">⇧</a>Table Address.Address</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Address"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Address"></span>AddressId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">varchar (100)</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Line1</th>
            <td class="type">varchar (100)</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Line2</th>
            <td class="type">varchar (50)</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Line3</th>
            <td class="type">varchar (50)</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>City</th>
            <td class="type">varchar (100)</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>State</th>
            <td class="type">varchar (2)</td>
            <td class="null">☐</td>
            <td>State code</td>
          </tr>
          <tr>
            <th></th>
            <th>ZipCode</th>
            <td class="type">varchar (25)</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Country</th>
            <td class="type">varchar (2)</td>
            <td class="null">☐</td>
            <td>Contry code</td>
          </tr>
          <tr>
            <th></th>
            <th>AddressTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1509580416"><a href="#toc" class="tocref">⇧</a>Table Address.AddressType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_AddressType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_AddressType"></span>AddressTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1323151759"><a href="#toc" class="tocref">⇧</a>Table Address.Country</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th></th>
            <th>CountryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1355151873"><a href="#toc" class="tocref">⇧</a>Table Address.StateProvince</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_StateProvince"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_StateProvince"></span>StateProvinceId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CountryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1156199169"><a href="#toc" class="tocref">⇧</a>Table Company.Company</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Company"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Company"></span>CompanyId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AccountNumber</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1108198998"><a href="#toc" class="tocref">⇧</a>Table Company.Contact</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Contact"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Contact"></span>ContactId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>PersonId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AddressId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Notes</th>
            <td class="type">varchar (250)</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="807673925"><a href="#toc" class="tocref">⇧</a>Table Company.Department</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Department"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Department"></span>DepartmentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ParentDepartmentId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2055678371"><a href="#toc" class="tocref">⇧</a>Table Company.Division</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Division"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Division"></span>DivisionId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="178099675"><a href="#toc" class="tocref">⇧</a>Table Company.Employee</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Employee"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Employee"></span>EmployeeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="226099846"><a href="#toc" class="tocref">⇧</a>Table Company.EmployeeCategory</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_EmployeeCategory"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_EmployeeCategory"></span>EmployeeCategoryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="478624748"><a href="#toc" class="tocref">⇧</a>Table Company.EmployeeRole</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_EmployeeRole"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_EmployeeRole"></span>EmployeeRoleId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1198627313"><a href="#toc" class="tocref">⇧</a>Table Company.Note</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Notes"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Notes"></span>NotesId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="430624577"><a href="#toc" class="tocref">⇧</a>Table Company.Role</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Role"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Role"></span>RoleId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="4195065"><a href="#toc" class="tocref">⇧</a>Table Company.Setting</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Setting"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Setting"></span>SettingId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1300199682"><a href="#toc" class="tocref">⇧</a>Table dbo.InventoryMethod</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryMethod"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryMethod"></span>InventoryMethodId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td> FIFO,  LIFO, FIFO,  LIFO</td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1934629935"><a href="#toc" class="tocref">⇧</a>Table Inventory.Adjustment</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Adjustment"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Adjustment"></span>AdjustmentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Note</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AdjustmentTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2030630277"><a href="#toc" class="tocref">⇧</a>Table Inventory.AdjustmentLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_AdjustmentLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_AdjustmentLine"></span>AdjustmentLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Quantity</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UnitCost</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AdjustmentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="946102411"><a href="#toc" class="tocref">⇧</a>Table Inventory.Incoterms</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Incoterms"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Incoterms"></span>IncotermsId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="898102240"><a href="#toc" class="tocref">⇧</a>Table Inventory.Inventory</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Inventory"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Inventory"></span>InventoryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="994102582"><a href="#toc" class="tocref">⇧</a>Table Inventory.InventoryLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryLine"></span>InventoryLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="619149251"><a href="#toc" class="tocref">⇧</a>Table Inventory.Item</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Item"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Item"></span>ItemId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LongDescription</th>
            <td class="type">text</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Temperature</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>SKU</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UPC</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ImageUrl</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Cost</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Price</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Active</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Weight</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Width</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Height</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Length</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1911677858"><a href="#toc" class="tocref">⇧</a>Table Inventory.ItemType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryItem"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryItem"></span>ItemTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="574625090"><a href="#toc" class="tocref">⇧</a>Table Inventory.StockQuantityHistory</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_StockQuantityHistory"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_StockQuantityHistory"></span>StockQuantityHistoryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1767677345"><a href="#toc" class="tocref">⇧</a>Table Inventory.TransferOrder</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_TransferOrder"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_TransferOrder"></span>TransferOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="334624235"><a href="#toc" class="tocref">⇧</a>Table Log.ActivityLog</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ActivityLog"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ActivityLog"></span>ActivityLogId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="382624406"><a href="#toc" class="tocref">⇧</a>Table Log.ActivityLogType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ActivityLogType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ActivityLogType"></span>ActivityLogTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="628197288"><a href="#toc" class="tocref">⇧</a>Table Log.InventoryLog</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryLog"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_InventoryLog"></span>InventoryLogId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="526624919"><a href="#toc" class="tocref">⇧</a>Table Log.TransactionLog</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_TransactionLog"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_TransactionLog"></span>TransactionLogId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1204199340"><a href="#toc" class="tocref">⇧</a>Table Manufacturing.Assembly</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Assembly"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Assembly"></span>AssemblyId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1252199511"><a href="#toc" class="tocref">⇧</a>Table Manufacturing.AssemblyDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_AssemblyDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_AssemblyDetail"></span>AssemblyDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="964198485"><a href="#toc" class="tocref">⇧</a>Table Manufacturing.Bom</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Bom"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Bom"></span>BomId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Active</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Notes</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="836198029"><a href="#toc" class="tocref">⇧</a>Table Manufacturing.BomItem</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_BomItem"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_BomItem"></span>BomItemId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Quantity</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Active</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Instructions</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LongInstructions</th>
            <td class="type">text</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="884198200"><a href="#toc" class="tocref">⇧</a>Table Manufacturing.BomItemType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_BomItemType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_BomItemType"></span>BomItemTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1396200024"><a href="#toc" class="tocref">⇧</a>Table Person.Person</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Person"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Person"></span>PersonId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>PersonType</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>CU = Individual customer, SP = Sales person, EM = Employee, VD = Vendor, GE = General entity, DV = Driver</td>
          </tr>
          <tr>
            <th></th>
            <th>Title</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>FirstName</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>MiddleName</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LastName</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Suffix</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Birthday</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Gender</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="466100701"><a href="#toc" class="tocref">⇧</a>Table Pointofsale.PosConfiguration</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PosConfiguration"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PosConfiguration"></span>PosConfigurationId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="418100530"><a href="#toc" class="tocref">⇧</a>Table Pointofsale.PosDiscount</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PosDiscount"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PosDiscount"></span>PosDiscountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="370100359"><a href="#toc" class="tocref">⇧</a>Table Pointofsale.PosOrder</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PosOrder"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PosOrder"></span>PosOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="322100188"><a href="#toc" class="tocref">⇧</a>Table Pointofsale.PosOrderLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PosOrderLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PosOrderLine"></span>PosOrderLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="802101898"><a href="#toc" class="tocref">⇧</a>Table Product.Attribute</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Attribute"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Attribute"></span>AttributeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="850102069"><a href="#toc" class="tocref">⇧</a>Table Product.AttributeLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_AttributeLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_AttributeLine"></span>AttributeLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="610101214"><a href="#toc" class="tocref">⇧</a>Table Product.Category</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Category"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Category"></span>CategoryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="658101385"><a href="#toc" class="tocref">⇧</a>Table Product.Image</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Image"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Image"></span>ImageId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1527676490"><a href="#toc" class="tocref">⇧</a>Table Product.KitItem</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_KitItem"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_KitItem"></span>KitItemId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Manufacturer</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Weight</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>WeightUnit</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ParentId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="388196433"><a href="#toc" class="tocref">⇧</a>Table Product.KitItemType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_KitItemType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_KitItemType"></span>KitItemTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1858105660"><a href="#toc" class="tocref">⇧</a>Table Product.Manufacturer</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Manufacturer"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Manufacturer"></span>ManufacturerId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="238623893"><a href="#toc" class="tocref">⇧</a>Table Product.MeasureDimension</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_MeasureDimension"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_MeasureDimension"></span>MeasureDimensionId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="286624064"><a href="#toc" class="tocref">⇧</a>Table Product.MeasureWeight</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_MeasureWeight"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_MeasureWeight"></span>MeasureWeightId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1006626629"><a href="#toc" class="tocref">⇧</a>Table Product.Package</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Package"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Package"></span>PackageId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1060198827"><a href="#toc" class="tocref">⇧</a>Table Product.PricingRule</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PricingRule"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PricingRule"></span>PricingRuleId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>StartDate</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>EndDate</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="27147142"><a href="#toc" class="tocref">⇧</a>Table Product.Product</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Product"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Product"></span>ProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LongDescription</th>
            <td class="type">text</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Cost</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Price</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Active</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Weight</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Width</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Height</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Length</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1403152044"><a href="#toc" class="tocref">⇧</a>Table Product.ProductAttribute</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductAttribute"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductAttribute"></span>ProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductAttribute"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductAttribute"></span>AttributeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="651149365"><a href="#toc" class="tocref">⇧</a>Table Product.ProductImage</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductImage"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductImage"></span>ProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductImage"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductImage"></span>ImageId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1810105489"><a href="#toc" class="tocref">⇧</a>Table Product.ProductReview</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductReview"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductReview"></span>ProductReviewId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="754101727"><a href="#toc" class="tocref">⇧</a>Table Product.ProductTaxes</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductTaxes"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductTaxes"></span>ProductTaxesId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1483152329"><a href="#toc" class="tocref">⇧</a>Table Product.RelatedProduct</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_RelatedProduct"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_RelatedProduct"></span>RelatedProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>ParentProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ProductId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="706101556"><a href="#toc" class="tocref">⇧</a>Table Product.Template</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Template"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Template"></span>TemplateId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="859150106"><a href="#toc" class="tocref">⇧</a>Table Product.Vehicle</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Vehicle"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Vehicle"></span>VehicleId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>VIN</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>VehicleDefinitionId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="939150391"><a href="#toc" class="tocref">⇧</a>Table Product.VehicleDefinition</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_VehicleDefinition"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_VehicleDefinition"></span>VehicleDefinitionId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Make</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Model</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Year</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Body</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>WeightUnitKG</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>LengthtUnitMM</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>WidthUnitMM</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>HeightUnitMM</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="327672215"><a href="#toc" class="tocref">⇧</a>Table Purchasing.PurchaseOrder</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PurchaseOrder"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PurchaseOrder"></span>PurchaseOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>Closed, Billed, Received, Receipt, Pending</td>
          </tr>
          <tr>
            <th></th>
            <th>TotalQuantity</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>TaxTotal</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>SubTotal</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Total</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>DueDate</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Memo</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ReferenceNumber</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ShippingDate</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ShippingMethodId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>BillingAddressId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ShippingAddressId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ShipToId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>EmployeeId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>VendorId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="539148966"><a href="#toc" class="tocref">⇧</a>Table Purchasing.PurchaseOrderDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PurchaseOrderDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PurchaseOrderDetail"></span>PurchaseOrderDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Quantity</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UnitCost</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>PurchaseOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="763149764"><a href="#toc" class="tocref">⇧</a>Table Purchasing.Vendor</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Vendor"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Vendor"></span>VendorId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1671677003"><a href="#toc" class="tocref">⇧</a>Table Reporting.ExpenseReport</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ExpenseReport"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ExpenseReport"></span>ExpenseReportId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="683149479"><a href="#toc" class="tocref">⇧</a>Table Sales.Customer</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Customer"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Customer"></span>CustomerId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span>Primary key.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="52195236"><a href="#toc" class="tocref">⇧</a>Table Sales.ProductService</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ProductService"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ProductService"></span>ProductServiceId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1714105147"><a href="#toc" class="tocref">⇧</a>Table Sales.Quotation</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Quote"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Quote"></span>QuotationId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1762105318"><a href="#toc" class="tocref">⇧</a>Table Sales.QuotationDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_QuoteDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_QuoteDetail"></span>QuotationDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="75147313"><a href="#toc" class="tocref">⇧</a>Table Sales.SalesOrder</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_SalesOrder"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_SalesOrder"></span>SalesOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>The status of the order. Options: pending, open, canceled, closed, completed</td>
          </tr>
          <tr>
            <th></th>
            <th>SalesPersonId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedByUserId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2126630619"><a href="#toc" class="tocref">⇧</a>Table Sales.SalesOrderDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_SalesOrderLineId"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_SalesOrderLineId"></span>SalesOrderDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Quantity</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>UnitCost</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>TotalTax</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1173579219"><a href="#toc" class="tocref">⇧</a>Table Sales.SalesPerson</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_SalesPerson"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_SalesPerson"></span>SalesPersonId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1125579048"><a href="#toc" class="tocref">⇧</a>Table Sales.SalesTaxRate</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_SalesTaxRate"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_SalesTaxRate"></span>SalesTaxRateId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1077578877"><a href="#toc" class="tocref">⇧</a>Table Sales.SpecialOffer</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_SpecialOffer"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_SpecialOffer"></span>SpecialOfferId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="340196262"><a href="#toc" class="tocref">⇧</a>Table Shipping.Airline</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Airline"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Airline"></span>AirlineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1131151075"><a href="#toc" class="tocref">⇧</a>Table Shipping.Booking</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CargoRelease"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CargoRelease"></span>BookingId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1275151588"><a href="#toc" class="tocref">⇧</a>Table Shipping.BookingDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CargoReleaseDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CargoReleaseDetail"></span>BookingDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CargoReleaseId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="676197459"><a href="#toc" class="tocref">⇧</a>Table Shipping.Carrier</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Carrier"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Carrier"></span>CarrierId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="772197801"><a href="#toc" class="tocref">⇧</a>Table Shipping.CarrierService</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CarrierService"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CarrierService"></span>CarrierServiceId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CarrierId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2103678542"><a href="#toc" class="tocref">⇧</a>Table Shipping.Port</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Port"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Port"></span>PortId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2050106344"><a href="#toc" class="tocref">⇧</a>Table Shipping.Return</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Return"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Return"></span>ReturnId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2098106515"><a href="#toc" class="tocref">⇧</a>Table Shipping.ReturnRequest</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ReturnRequest"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ReturnRequest"></span>ReturnRequestId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="94623380"><a href="#toc" class="tocref">⇧</a>Table Shipping.ReturnRequestAction</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ReturnRequestAction"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ReturnRequestAction"></span>ReturnRequestActionId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="46623209"><a href="#toc" class="tocref">⇧</a>Table Shipping.ReturnRequestReason</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ReturnRequestReason"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ReturnRequestReason"></span>ReturnRequestReasonId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1035150733"><a href="#toc" class="tocref">⇧</a>Table Shipping.Route</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Route"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Route"></span>RouteId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1522104463"><a href="#toc" class="tocref">⇧</a>Table Shipping.Shipment</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Shipment"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Shipment"></span>ShipmentId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1570104634"><a href="#toc" class="tocref">⇧</a>Table Shipping.ShipmentDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ShipmentDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ShipmentDetail"></span>ShipmentDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="148195578"><a href="#toc" class="tocref">⇧</a>Table Shipping.ShippingLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingLine"></span>ShippingLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>SCACCode</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Code</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Website</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Inactive</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Notes</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="190623722"><a href="#toc" class="tocref">⇧</a>Table Shipping.ShippingMethod</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingMethod"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingMethod"></span>ShippingMethodId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="142623551"><a href="#toc" class="tocref">⇧</a>Table Shipping.ShippingMethodRestrictions</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingMethodRestrictions"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingMethodRestrictions"></span>ShippingMethodRestrictionsId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1435152158"><a href="#toc" class="tocref">⇧</a>Table Shipping.ShippingRate</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingRate"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingRate"></span>ShippingRateId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Active</th>
            <td class="type">boolean</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="532196946"><a href="#toc" class="tocref">⇧</a>Table Shipping.ShippingTerms</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingTerms"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ShippingTerms"></span>ShippingTermsId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="987150562"><a href="#toc" class="tocref">⇧</a>Table Shipping.Trip</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Trip"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Trip"></span>TripId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="292196091"><a href="#toc" class="tocref">⇧</a>Table System.Backup</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Backup"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Backup"></span>BackupId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Type</th>
            <td class="type">character varying</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1806629479"><a href="#toc" class="tocref">⇧</a>Table System.Cache</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Cache"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Cache"></span>CacheId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Data</th>
            <td class="type">text</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ExpireOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="622625261"><a href="#toc" class="tocref">⇧</a>Table System.Configuration</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Configuration"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Configuration"></span>ConfigurationId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="718625603"><a href="#toc" class="tocref">⇧</a>Table System.ConfigurationDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ConfigurationDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ConfigurationDetail"></span>ConfigurationDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="814625945"><a href="#toc" class="tocref">⇧</a>Table System.Event</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Event"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Event"></span>EventId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="862626116"><a href="#toc" class="tocref">⇧</a>Table System.EventType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_EventType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_EventType"></span>EventTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="766625774"><a href="#toc" class="tocref">⇧</a>Table System.Installer</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Installer"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Installer"></span>InstallerId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="670625432"><a href="#toc" class="tocref">⇧</a>Table System.Language</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Language"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Language"></span>LanguageId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1294627655"><a href="#toc" class="tocref">⇧</a>Table System.Maintenance</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Maintenance"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Maintenance"></span>MaintenanceId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1342627826"><a href="#toc" class="tocref">⇧</a>Table System.Preferences</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Preferences"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Preferences"></span>PreferencesId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1348199853"><a href="#toc" class="tocref">⇧</a>Table System.UserReminder</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_UserReminder"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_UserReminder"></span>UserReminderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1479676319"><a href="#toc" class="tocref">⇧</a>Table Transactions.CashRefund</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CashRefund"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CashRefund"></span>CashRefundId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="279672044"><a href="#toc" class="tocref">⇧</a>Table Transactions.Check</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Check"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Check"></span>CheckId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Number</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Amount</th>
            <td class="type">numeric</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Memo</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>ToBePrinted</th>
            <td class="type">boolean</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AccountId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>PayeeId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>CurrencyId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1618104805"><a href="#toc" class="tocref">⇧</a>Table Transactions.CreditMemo</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_CreditMemo"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_CreditMemo"></span>CreditMemoId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="855674096"><a href="#toc" class="tocref">⇧</a>Table Transactions.Job</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Job"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Job"></span>JobId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="903674267"><a href="#toc" class="tocref">⇧</a>Table Transactions.JobType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_JobType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_JobType"></span>JobTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="951674438"><a href="#toc" class="tocref">⇧</a>Table Transactions.JournalEntry</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_JournalEntry"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_JournalEntry"></span>JournalEntryId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1335675806"><a href="#toc" class="tocref">⇧</a>Table Transactions.Task</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Task"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Task"></span>TaskId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Name</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>Status</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>NotStarted, Pending, InProgress, Completed</td>
          </tr>
          <tr>
            <th></th>
            <th>Priority</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>High, Low, Medium</td>
          </tr>
          <tr>
            <th></th>
            <th>DueDate</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>StartDate</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>EndDate</th>
            <td class="type">date</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>AssignedToId</th>
            <td class="type">integer</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1186103266"><a href="#toc" class="tocref">⇧</a>Table Warehousing.Location</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Location"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Location"></span>LocationId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1234103437"><a href="#toc" class="tocref">⇧</a>Table Warehousing.LocationRoute</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_LocationRoute"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_LocationRoute"></span>LocationRouteId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="436196604"><a href="#toc" class="tocref">⇧</a>Table Warehousing.LocationType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_LocationType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_LocationType"></span>LocationTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Description</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1282103608"><a href="#toc" class="tocref">⇧</a>Table Warehousing.Move</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Move"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Move"></span>MoveId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1330103779"><a href="#toc" class="tocref">⇧</a>Table Warehousing.MoveLine</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_MoveLine"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_MoveLine"></span>MoveLineId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1090102924"><a href="#toc" class="tocref">⇧</a>Table Warehousing.Picking</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Picking"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Picking"></span>PickingId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1138103095"><a href="#toc" class="tocref">⇧</a>Table Warehousing.PickingType</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PickingType"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PickingType"></span>PickingTypeId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1083150904"><a href="#toc" class="tocref">⇧</a>Table Warehousing.PickupOrder</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PickupOrder"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PickupOrder"></span>PickupOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1227151417"><a href="#toc" class="tocref">⇧</a>Table Warehousing.PickupOrderDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_PickupOrderDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_PickupOrderDetail"></span>PickupOrderDetailId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>PickupOrderId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="910626287"><a href="#toc" class="tocref">⇧</a>Table Warehousing.Receipt</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Receipt"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Receipt"></span>ReceiptId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="958626458"><a href="#toc" class="tocref">⇧</a>Table Warehousing.ReceiptDetail</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_ReceiptDetail"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_ReceiptDetail"></span>ReceipDetailtId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="2007678200"><a href="#toc" class="tocref">⇧</a>Table Warehousing.Release</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Release"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Release"></span>ReleaseId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>Number</th>
            <td class="type">character varying</td>
            <td class="null">☒</td>
            <td>
            </td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="table">
      <h2 id="1042102753"><a href="#toc" class="tocref">⇧</a>Table Warehousing.Warehouse</h2>
      <table>
        <thead>
          <tr>
            <th style="width:2ex"></th>
            <th style="width:30ex">Name</th>
            <th style="width:20ex">Data Type</th>
            <th style="width:12ex">Allow Nulls</th>
            <th>Desciption</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th><span class="pk" title="PRIMARY KEY PK_Warehouse"><img src="F:\CEDRUS LOGISTICS\DEV-01\Tools\Data\SqlDbDocumentation\SqlDbDoc\Resources\Templates\key-icon.png"></span></th>
            <th><span class="pk" title="PRIMARY KEY PK_Warehouse"></span>WarehouseId</th>
            <td class="type">integer</td>
            <td class="null">☐</td>
            <td><span class="flag">IDENTITY</span></td>
          </tr>
          <tr>
            <th></th>
            <th>RowGuid</th>
            <td class="type">uuid</td>
            <td class="null">☐</td>
            <td><span class="flag">DEFAULT (newid())</span>ROWGUIDCOL number uniquely identifying the record (to support a merge replication)</td>
          </tr>
          <tr>
            <th></th>
            <th>CreatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record was created.</td>
          </tr>
          <tr>
            <th></th>
            <th>UpdatedOnUtc</th>
            <td class="type">date</td>
            <td class="null">☐</td>
            <td>Date (Utc) and time the record last updated.</td>
          </tr>
        </tbody>
      </table>
    </div>
  </body>
</html>
