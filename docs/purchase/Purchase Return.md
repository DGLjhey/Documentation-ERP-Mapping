### AddPurchaseReturnV2
**Views**
```md title="File Location: "
@{
    ViewData["Title"] = "AddPurchaseReturnV2";
    Layout = "~/Views/Shared/_Layout.cshtml";
}

<link href="~/css/add-purchase-return.css" rel="stylesheet" />

<div class="purchaseReturnTitle">
    <h3>Create Purchase Return V2</h3>
    <div class="closeButton">
        <i class="fa fa-times"></i>
    </div>
</div>

<div class="purchaseReturnContainer">
    <div class="purchaseReturnCard">
        <div class="cardHeading">
            <label>B13PRTN-0000000001</label>
        </div>

        <div class="cardBody">
            <div class="bodyGrid">
                <div class="columnOne">
                    <div class="bodyInfo ui search">
                        <label>Supplier</label>
                        <div class="ui fluid icon input">
                            <input placeholder="Search by company" type="text" tabindex="0" class="prompt" autocomplete="off" value="">
                            <i aria-hidden="true" class="search icon"></i>
                        </div>

                        <div class="results transition">
                            <div class="message empty">
                                <div class="header">
                                    No results found.
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="bodyInfo">
                        <label for="departmentId">Department</label>
                        <div class="ui input">
                            <input type="text" value="">
                        </div>
                    </div>
                </div>

                <div class="columnTwo">
                    <div class="bodyInfo">
                        <label>Requested By:</label>
                        <label>SYSTEM ADMIN</label>
                    </div>

                    <div class="bodyInfo">
                        <label for="">Return From</label>
                        <div class="bodyDropdown">
                            <select id="" class="form form-control">
                                <option value="Purchase Order">Purchase Order</option>
                                <option value="Manual">Manual</option>
                            </select>
                        </div>
                    </div>

                    <div class="bodyInfo">
                        <label for="">Return Date</label>
                        <input type="date" value="" class="form form-control" required />
                    </div>
                </div>
            </div>

            @*For Table on Supplier Search*@
            @*<div class="tableContainer">
                <div class="addItemButton">
                    <button title="" class="ui blue mini icon left labeled button font-mini">
                        <i aria-hidden="true" class="add icon"></i>Add Item
                    </button>
                </div>

                
                <div class="table-responsive addPurchaseReturnTable">
                    <table class="table table-striped table-bordered" id="addPurchaseReturnTable" cellspacing="0" width="100%">
                        <colgroup>
                            <col style="width: 200px; min-width: 200px;">
                            <col style="width: 100px; min-width: 100px;">
                            <col style="width: 70px; min-width: 70px;">
                            <col style="width: 150px; min-width: 150px;">
                            <col style="width: 200px; min-width: 200px;">
                            <col style="width: 150px; min-width: 150px;">
                            <col style="width: 200px; min-width: 200px;">
                            <col style="width: 235px; min-width: 235px;">
                            <col style="width: 140px; min-width: 140px;">
                            <col style="width: 35px; min-width: 35px;">
                        </colgroup>

                        <thead>
                            <tr>
                                <th>Item Name</th>
                                <th>Item Code</th>
                                <th>UOM</th>
                                <th>Return Qty</th>
                                <th>Return Reason</th>
                                <th>Expiration Date</th>
                                <th>Warehouse From</th>
                                <th>Location From</th>
                                <th>Stock on Hand</th>
                                <th>Action</th>
                            </tr>
                        </thead>

                        <tbody>
                            <tr>
                                <td>
                                    <div class="input-group border rounded">
                                        <input class="form-control shadow-none border-0" type="text" name="itemName" placeholder="Search by item name or item code">
                                        <span class="input-group-append">
                                            <button class="btn bg-transparent ms-3" type="button" disabled>
                                                <i class="fa fa-search"></i>
                                            </button>
                                        </span>
                                    </div>
                                </td>

                                <td>For Item Code</td>
                                <td>For UOM</td>

                                <td>
                                    <div class="input-group">
                                        <input type="number" class="form-control" name="quantity" placeholder="0" />
                                    </div>
                                </td>

                                <td>
                                    <div class="input-group">
                                        <select name="returnReason" class="form-control">
                                            <option disabled selected hidden></option>
                                            <option>Sample 1</option>
                                            <option>Sample 2</option>
                                            <option>Sample 3</option>
                                            <option>Sample 4</option>
                                        </select>
                                    </div>
                                </td>

                                <td>
                                    <div class="input-group">
                                        <input type="date" class="form-control" name="expirationDate" />
                                    </div>
                                </td>

                                <td class="text-right">
                                    <label>No Warehouses Available</label>
                                </td>

                                <td class="text-right">
                                    <label>No Locations Available</label>
                                </td>

                                <td class="text-right">
                                    <label>0</label>
                                </td>

                                <td>
                                    <div class="input-group d-flex justify-content-center align-items-center">
                                        <button type="button" class="btn btn-danger delete-row">
                                            <i class="fa fa-times"></i>
                                        </button>
                                    </div>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>*@
            
            <div class="remarks">
                <label>Remarks</label>
                <textarea class="form form-control" placeholder="Type your remarks here..." rows="6"></textarea>
            </div>

            <div class="tableButtons">
                <button type="button" title="" class="ui green mini icon disabled left labeled button" disabled="" tabindex="-1">
                    <i aria-hidden="true" class="save icon"></i>Save As Draft
                </button>

                <button type="button" title="" class="ui blue mini icon disabled left labeled button" disabled="" tabindex="-1">
                    <i aria-hidden="true" class="save icon"></i>Submit
                </button>

                <button type="button" title="" class="ui red mini icon left labeled button" data-toggle="modal" data-target="#cancelModal">
                    <i aria-hidden="true" class="cancel icon"></i>Cancel
                </button>
            </div>

            <!-- Modal -->
            <div class="modal fade" id="cancelModal" tabindex="-1" role="dialog" aria-labelledby="cancelModalLabel" aria-hidden="true">
                <div class="modal-dialog" role="document">
                    <div class="modal-content">
                        <div class="modal-header modalTitleSize">
                            <h5 class="modal-title" id="cancelModalLabel">Confirmation</h5>
                            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                                <span aria-hidden="true">&times;</span>
                            </button>
                        </div>
                        <div class="modal-body modalBodySize">
                            Are you sure you want to cancel?
                        </div>
                        <div class="modal-footer">
                            <button class="ui green mini icon left labeled button">
                                <i aria-hidden="true" class="checkmark icon"></i>Yes
                            </button>
                            
                            <button class="ui red mini icon left labeled button" data-dismiss="modal">
                                <i aria-hidden="true" class="cancel icon"></i>No
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    $(document).ready(function () {
        $('#addPurchaseReturnTable').DataTable({
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
            dom: "",
        });
    });
</script>
```

**Controllers**
```md title="File Location: "
public IActionResult AddPurchaseReturnV2()
        {
            return View("~/Views/Purchase/PurchaseReturn/AddPurchaseReturnV2.cshtml");
        }

```