### AddPurchaseRequestV2
**Views**
```md title="File Location: Views/Purchase/PurchaseRequest/AddPurchaseRequestV2.cshtml"

@{
    ViewData["Title"] = "AddPurchaseRequestV2";
    Layout = "~/Views/Shared/_Layout.cshtml";
}

@*========== Header of the Page ==========*@
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3>New Purchase Request</h3>
        </div>
        <div class="col-md-6 card-body text-right">
            <a href="#">
                <h3><i class="fa fa-times"></i><span class="cui-contrast"></span></h3>
            </a>
        </div>
    </div>
</div>
@*========== Body of the Page ==========*@
<div class="container-fluid">
    <div class="row justify-content-center mt-4">
        <div class="col-lg-12 col-md-8 col-sm-10">
            @*First Card*@
            <div class="card">
                @*Header of the Card*@
                <header class="bg-primary p-2 d-flex justify-content-end">
                    <h5>PR-0000000414</h5>
                </header>
                <div class="card-body">
                    <main class="row">
                        @*First Column of the Card*@
                        <div class="col-lg-4 col-md-12 col-sm-12">
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="department" class="font-weight-bolder">Department:</label>
                                </div>
                                <div class="col-8">
                                    <select id="department" name="department" class="form-control" aria-label="Select department">
                                        <option disabled selected hidden></option>
                                        <option>Sample 1</option>
                                        <option>Sample 2</option>
                                        <option>Sample 3</option>
                                        <option>Sample 4</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                        @*Second Column of the Card*@
                        <div class="col-lg-4 col-md-12 col-sm-12">
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="deliver-to" class="font-weight-bolder">Deliver To:</label>
                                </div>
                                <div class="col-8">
                                    <select id="deliver-to" name="deliver-to" class="form-control" aria-label="Select delivery location">
                                        <option disabled selected hidden></option>
                                        <option>Sample 1</option>
                                        <option>Sample 2</option>
                                        <option>Sample 3</option>
                                        <option>Sample 4</option>
                                    </select>
                                </div>
                            </div>
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="date-needed" class="font-weight-bolder">Date Needed:</label>
                                </div>
                                <div class="col-8">
                                    <input id="date-needed" name="date-needed" type="date" class="form-control" aria-label="Select date needed">
                                </div>
                            </div>
                        </div>
                        @*Third Column of the Card*@
                        <div class="col-lg-4 col-md-12 col-sm-12">
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="requested-by" class="font-weight-bolder">Requested By:</label>
                                </div>
                                <div class="col-8">
                                    <p id="requested-by">SYSTEM ADMIN</p>
                                </div>
                            </div>
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="pr-date" class="font-weight-bolder">PR Date:</label>
                                </div>
                                <div class="col-8">
                                    <p id="pr-date">03/30/2023</p>
                                </div>
                            </div>
                        </div>
                        @*Last Column of the Card*@
                        <div class="col-12">
                            <label class="font-weight-bolder">Remarks:</label>
                            <textarea class="form-control border-0 shadow-none" placeholder="Type your remarks here"></textarea>
                        </div>
                    </main>
                </div>
            </div>
            @*Second Card*@
            <div class="card">
                <div class="card-body">
                    @*Add Item Button Area*@
                    <header class="row">
                        <div class="col-12 mb-2">
                            @*Add Item Button Trigger Modal*@
                            <button type="button" class="btn btn-primary float-right" data-toggle="modal" data-target="#addItemModal"><i class="fa fa-plus pr-2"></i> Add Item</button> 
                        </div>
                    </header>
                    @*Table Area*@
                    <main class="row">
                        <section class="col-12">
                            <table id="items-table" class="table table-bordered">
                                <thead>
                                    <tr>
                                        <th scope="col" class="col-1">No</th>
                                        <th scope="col" class="col-3">Item Name</th>
                                        <th scope="col" class="col-3">Item Code</th>
                                        <th scope="col" class="col-2">Quantity</th>
                                        <th scope="col" class="col-2">Unit</th>
                                        <th scope="col" class="col-1">Action</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td colspan="6" class="text-center">there is no data to display</td>
                                    </tr>
                                    <tr class="table-secondary">
                                        <td></td>
                                        <td class="font-weight-bolder">Total</td>
                                        <td></td>
                                        <td class="font-weight-bolder">0</td>
                                        <td></td>
                                        <td></td>
                                    </tr>
                                </tbody>
                            </table>
                        </section>
                    </main>
                </div>
            </div>
            @*The 3 buttons on the lower right of the card (Outside)*@
            <div class="float-right">
                @*Save Button Trigger Modal*@
                <button type="button" class="btn btn-success" data-toggle="modal" data-target="#saveModal"><i class="fa fa-bookmark pr-2"></i> Save as Draft</button>
                @*Submit Button Trigger Modal*@
                <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#submitModal"><i class="fa fa-upload pr-2"></i> Submit</button>
                @*Cancel Button Trigger Modal*@
                <button type="button" class="btn btn-danger" data-toggle="modal" data-target="#cancelModal"><i class="fa fa-times pr-2"></i> Cancel</button>


                @*=============== M O D A L S ===============*@

                @*==========Add Item Button Modal==========*@
                <div class="modal fade" id="addItemModal" tabindex="-1" role="dialog" aria-labelledby="addItemModalLabel" aria-hidden="true">
                    <div class="modal-dialog modal-lg" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="addItemModalLabel">Add Item</h2>
                            </div>
                            <div class="modal-body">
                                <div class="row">
                                    <div class="col-12 mb-2">
                                        <button id="add-item-btn" type="button" class="btn btn-primary float-right"><i class="fa fa-plus pr-2"></i> Add Item</button>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-12">
                                        <table id="itemsTable" class="table table-bordered">
                                            <thead>
                                                <tr>
                                                    <th scope="col" class="col-6">Item Name</th>
                                                    <th scope="col" class="col-2">Item Code</th>
                                                    <th scope="col" class="col-1">Quantity</th>
                                                    <th scope="col" class="col-2">OUM</th>
                                                    <th scope="col" class="col-1"></th>
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
                                                    <td>@*For Item Code<*@</td>
                                                    <td><input type="number" class="form-control" name="quantity" placeholder="0" /></td>
                                                    <td>
                                                        <select name="uom" class="form-control">
                                                            <option disabled selected hidden></option>
                                                            <option>Sample 1</option>
                                                            <option>Sample 2</option>
                                                            <option>Sample 3</option>
                                                            <option>Sample 4</option>
                                                        </select>
                                                    </td>
                                                    <td class="text-center"><button type="button" class="btn btn-danger delete-row"><i class="fa fa-times"></i></button></td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                </div>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Add</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> Close</button>
                            </div>
                        </div>
                    </div>
                </div>

                @*==========Save Button Modal==========*@
                <div class="modal fade" id="saveModal" tabindex="-1" role="dialog" aria-labelledby="saveModalLabel" aria-hidden="true">
                    <div class="modal-dialog" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="saveModalLabel">Confirmation</h2>
                            </div>
                            <div class="modal-body">
                                <p class="fs-3">Are you sure you want to save as draft?</p>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Yes</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> No</button>
                            </div>
                        </div>
                    </div>
                </div>
                @*==========Submit Button Modal==========*@
                <div class="modal fade" id="submitModal" tabindex="-1" role="dialog" aria-labelledby="submitModalLabel" aria-hidden="true">
                    <div class="modal-dialog" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="submitModalLabel">Confirmation</h2>
                            </div>
                            <div class="modal-body">
                                <p class="fs-3">Are you sure you want to submit?</p>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Yes</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> No</button>
                            </div>
                        </div>
                    </div>
                </div>
                @*==========Cancel Button Modal==========*@
                <div class="modal fade" id="cancelModal" tabindex="-1" role="dialog" aria-labelledby="cancelModalLabel" aria-hidden="true">
                    <div class="modal-dialog" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="cancelModalLabel">Confirmation</h2>
                            </div>
                            <div class="modal-body">
                                <p class="fs-3">Are you sure you want to cancel?</p>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Yes</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> No</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    $(document).ready(function () {
        // Add row to table when "Add Item" button is clicked
        $("#add-item-btn").on("click", function () {
            var newRow = '<tr>' +
                '<td><div class="input-group border rounded"><input class="form-control shadow-none border-0" type="text" name="itemName" placeholder="Search by item name or item code"><span class="input-group-append"><button class="btn bg-transparent ms-3" type="button" disabled><i class="fa fa-search"></i></button></span></div></td>' +
                '<td></td>' +
                '<td><input type="number" class="form-control" name="quantity" placeholder="0"/></td>' +
                '<td><select name="uom" class="form-control"><option disabled selected hidden></option><option>Sample 1</option><option>Sample 2</option><option>Sample 3</option><option>Sample 4</option></select></td>' +
                '<td class="text-center"><button type="button" class="btn btn-danger delete-row"><i class="fa fa-times"></i></button></td>' +
                '</tr>';
            $("#itemsTable tbody").append(newRow);
        });

        // Delete row from table when "Delete" button is clicked
        $("#itemsTable").on("click", ".delete-row", function () {
            $(this).closest("tr").remove();
        });
    });
        //For DataTable
        //$(document).ready(function () {

        //    $('#items-table').DataTable({
        //        dom: "<'myfilter'f><'mylength'l>tip",
        //        ordering: true,
        //        select: {
        //            selector: 'td:not(:first-child)',
        //            style: 'os'
        //        },
        //    });
        //});
</script>

```

**Controllers**
```md title="File Location: Controllers/Purchase/PurchaseRequest/PurchaseRequestController.cs"
public IActionResult AddPurchaseRequestV2()
        {
            
            return View("~/Views/Purchase/PurchaseRequest/AddPurchaseRequestV2.cshtml");
        }
```


### EditPurchaseRequestV2
**Views**
```md title="File Location: View/Purchase/PurchaseRequest/EditPurchaseRequestV2.cshtml"

@{
    ViewData["Title"] = "EditPurchaseRequestV2";
    Layout = "~/Views/Shared/_Layout.cshtml";
}

@*========== Header of the Page ==========*@
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3>Edit Purchase Request</h3>
        </div>
        <div class="col-md-6 card-body text-right">
            <a href="#">
                <h3><i class="fa fa-times"></i><span class="cui-contrast"></span></h3>
            </a>
        </div>
    </div>
</div>
@*========== Body of the Page ==========*@
<div class="container-fluid">
    <div class="row justify-content-center mt-4">
        <div class="col-lg-12 col-md-8 col-sm-10">
            @*First Card*@
            <div class="card">
                @*Header of the Card*@
                <header class="bg-primary p-2 d-flex justify-content-end">
                    <h5>PR-0000000413</h5>
                </header>
                <div class="card-body">
                    <main class="row">
                        @*First Column of the Card*@
                        <div class="col-lg-4 col-md-12 col-sm-12">
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="department" class="font-weight-bolder">Department:</label>
                                </div>
                                <div class="col-8">
                                    <select id="department" name="department" class="form-control" aria-label="Select department">
                                        <option disabled selected hidden></option>
                                        <option>Sample 1</option>
                                        <option>Sample 2</option>
                                        <option>Sample 3</option>
                                        <option>Sample 4</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                        @*Second Column of the Card*@
                        <div class="col-lg-4 col-md-12 col-sm-12">
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="deliver-to" class="font-weight-bolder">Deliver To:</label>
                                </div>
                                <div class="col-8">
                                    <select id="deliver-to" name="deliver-to" class="form-control" aria-label="Select delivery location">
                                        <option disabled selected hidden></option>
                                        <option>Sample 1</option>
                                        <option>Sample 2</option>
                                        <option>Sample 3</option>
                                        <option>Sample 4</option>
                                    </select>
                                </div>
                            </div>
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="date-needed" class="font-weight-bolder">Date Needed:</label>
                                </div>
                                <div class="col-8">
                                    <input id="date-needed" name="date-needed" type="date" class="form-control" aria-label="Select date needed">
                                </div>
                            </div>
                        </div>
                        @*Third Column of the Card*@
                        <div class="col-lg-4 col-md-12 col-sm-12">
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="requested-by" class="font-weight-bolder">Requested By:</label>
                                </div>
                                <div class="col-8">
                                    <p id="requested-by">SYSTEM ADMIN</p>
                                </div>
                            </div>
                            <div class="row pb-2">
                                <div class="col-4">
                                    <label for="pr-date" class="font-weight-bolder">PR Date:</label>
                                </div>
                                <div class="col-8">
                                    <p id="pr-date">03/30/2023</p>
                                </div>
                            </div>
                        </div>
                        @*Last Column of the Card*@
                        <div class="col-12">
                            <label class="font-weight-bolder">Remarks:</label>
                            <textarea class="form-control border-0 shadow-none" placeholder="Type your remarks here"></textarea>
                        </div>
                    </main>
                </div>
            </div>
            @*Second Card*@
            <div class="card">
                <div class="card-body">
                    @*Add Item Button Area*@
                    <header class="row">
                        <div class="col-12 mb-2">
                            @*Add Item Button Trigger Modal*@
                            <button type="button" class="btn btn-primary float-right" data-toggle="modal" data-target="#addItemModal"><i class="fa fa-plus pr-2"></i> Add Item</button> 
                        </div>
                    </header>
                    @*Table Area*@
                    <main class="row">
                        <section class="col-12">
                            <table id="items-table" class="table table-bordered">
                                <thead>
                                    <tr>
                                        <th scope="col" class="col-1">No</th>
                                        <th scope="col" class="col-3">Item Name</th>
                                        <th scope="col" class="col-3">Item Code</th>
                                        <th scope="col" class="col-2">Quantity</th>
                                        <th scope="col" class="col-2">Unit</th>
                                        <th scope="col" class="col-1">Action</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td>1</td>
                                        <td>CS-CHP-MWXS5K-P</td>
                                        <td>0701020605</td>
                                        <td>2,000</td>
                                        <td>pc</td>
                                        <td class="text-center"><button type="button" class="btn btn-danger delete-row"><i class="fa fa-times"></i></button></td>
                                    </tr>
                                    <tr class="table-secondary">
                                        <td></td>
                                        <td></td>
                                        <td></td>
                                        <td class="font-weight-bolder">2,000</td>
                                        <td></td>
                                        <td></td>
                                    </tr>
                                </tbody>
                            </table>
                        </section>
                    </main>
                </div>
            </div>
            @*The 3 buttons on the lower right of the card (Outside)*@
            <div class="float-right">
                @*Save Button Trigger Modal*@
                <button type="button" class="btn btn-success" data-toggle="modal" data-target="#saveModal"><i class="fa fa-bookmark pr-2"></i> Save as Draft</button>
                @*Submit Button Trigger Modal*@
                <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#submitModal"><i class="fa fa-upload pr-2"></i> Submit</button>
                @*Cancel Button Trigger Modal*@
                <button type="button" class="btn btn-danger" data-toggle="modal" data-target="#cancelModal"><i class="fa fa-times pr-2"></i> Cancel</button>
                

                @*=============== M O D A L S ===============*@

                @*==========Add Item Button Modal==========*@
                <div class="modal fade" id="addItemModal" tabindex="-1" role="dialog" aria-labelledby="addItemModalLabel" aria-hidden="true">
                    <div class="modal-dialog modal-lg" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="addItemModalLabel">Add Item</h2>
                            </div>
                            <div class="modal-body">
                                <div class="row">
                                    <div class="col-12 mb-2">
                                        <button id="add-item-btn" type="button" class="btn btn-primary float-right"><i class="fa fa-plus pr-2"></i> Add Item</button>
                                    </div>
                                </div>
                                <div class="row">
                                    <div class="col-12">
                                        <table id="itemsTable" class="table table-bordered">
                                            <thead>
                                                <tr>
                                                    <th scope="col" class="col-6">Item Name</th>
                                                    <th scope="col" class="col-2">Item Code</th>
                                                    <th scope="col" class="col-1">Quantity</th>
                                                    <th scope="col" class="col-2">OUM</th>
                                                    <th scope="col" class="col-1"></th>
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
                                                    <td>@*For Item Code<*@</td>
                                                    <td><input type="number" class="form-control" name="quantity" placeholder="0" /></td>
                                                    <td>
                                                        <select name="uom" class="form-control">
                                                            <option disabled selected hidden></option>
                                                            <option>Sample 1</option>
                                                            <option>Sample 2</option>
                                                            <option>Sample 3</option>
                                                            <option>Sample 4</option>
                                                        </select>
                                                    </td>
                                                    <td class="text-center"><button type="button" class="btn btn-danger delete-row"><i class="fa fa-times"></i></button></td>
                                                </tr>
                                            </tbody>
                                        </table>
                                    </div>
                                </div>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Add</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> Close</button>
                            </div>
                        </div>
                    </div>
                </div>

                @*==========Save Button Modal==========*@
                <div class="modal fade" id="saveModal" tabindex="-1" role="dialog" aria-labelledby="saveModalLabel" aria-hidden="true">
                    <div class="modal-dialog" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="saveModalLabel">Confirmation</h2>
                            </div>
                            <div class="modal-body">
                                <p class="fs-3">Are you sure you want to update?</p>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Yes</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> No</button>
                            </div>
                        </div>
                    </div>
                </div>
                @*==========Submit Button Modal==========*@
                <div class="modal fade" id="submitModal" tabindex="-1" role="dialog" aria-labelledby="submitModalLabel" aria-hidden="true">
                    <div class="modal-dialog" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="submitModalLabel">Confirmation</h2>
                            </div>
                            <div class="modal-body">
                                <p class="fs-3">Are you sure you want to submit?</p>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Yes</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> No</button>
                            </div>
                        </div>
                    </div>
                </div>
                @*==========Cancel Button Modal==========*@
                <div class="modal fade" id="cancelModal" tabindex="-1" role="dialog" aria-labelledby="cancelModalLabel" aria-hidden="true">
                    <div class="modal-dialog" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h2 class="modal-title" id="cancelModalLabel">Confirmation</h2>
                            </div>
                            <div class="modal-body">
                                <p class="fs-3">Are you sure you want to cancel?</p>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-success"><i class="fa fa-check pr-2"></i> Yes</button>
                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times pr-2"></i> No</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    $(document).ready(function () {
        // Add row to table when "Add Item" button is clicked
        $("#add-item-btn").on("click", function () {
            var newRow = '<tr>' +
                '<td><div class="input-group border rounded"><input class="form-control shadow-none border-0" type="text" name="itemName" placeholder="Search by item name or item code"><span class="input-group-append"><button class="btn bg-transparent ms-3" type="button" disabled><i class="fa fa-search"></i></button></span></div></td>' +
                '<td></td>' +
                '<td><input type="number" class="form-control" name="quantity" placeholder="0"/></td>' +
                '<td><select name="uom" class="form-control"><option disabled selected hidden></option><option>Sample 1</option><option>Sample 2</option><option>Sample 3</option><option>Sample 4</option></select></td>' +
                '<td class="text-center"><button type="button" class="btn btn-danger delete-row"><i class="fa fa-times"></i></button></td>' +
                '</tr>';
            $("#itemsTable tbody").append(newRow);
        });

        // Delete row from table when "Delete" button is clicked
        $("#itemsTable").on("click", ".delete-row", function () {
            $(this).closest("tr").remove();
        });
    });
        //For DataTable
        //$(document).ready(function () {

        //    $('#items-table').DataTable({
        //        dom: "<'myfilter'f><'mylength'l>tip",
        //        ordering: true,
        //        select: {
        //            selector: 'td:not(:first-child)',
        //            style: 'os'
        //        },
        //    });
        //});
</script>
```

**Controllers**
```md title="File Location: Controller/Purchase/PurchaseRequest/PurchaseRequestController.cs"
public IActionResult EditPurchaseRequestV2()
        {

            return View("~/Views/Purchase/PurchaseRequest/EditPurchaseRequestV2.cshtml");
        }
```
