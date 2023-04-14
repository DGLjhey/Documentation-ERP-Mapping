### CheckPreparationListV2
**Views**
```md title="File Location: Views/Purchase/CheckPreparation/CheckPreparationListV2.cshtml"
@*
    For more information on enabling MVC for empty projects, visit https://go.microsoft.com/fwlink/?LinkID=397860
*@
@{
}
@*
    For more information on enabling MVC for empty projects, visit https://go.microsoft.com/fwlink/?LinkID=397860
*@
@{
}
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3 class="pt-2">
                Prepared Checks
            </h3>
        </div>

        <div class="col-md-6 card-body text-right">
            <a class="btn btn-brand btn-behance" asp-controller="Checkpreparation" asp-action="addcheckpreparationv2"><i class="fa fa-plus-square"></i><span>Prepare New Check</span></a>
        </div>
    </div>
</div>
<div class="card ml-3 mr-3">
    <div class=" card-body" style="margin:0; padding: 0;">
        <ul class="nav nav-tabs">
            <li class="nav-item active" role="tablist">
                <button class="nav-link active h5 py-2 px-4" data-toggle="tab" id="forreleasing-tab" href="#forreleasing" role="tab">For Releasing<span class="ml-2 rounded" style="background-color: #2185d0 ; font-size: 12px; padding: 0px 10px 0px 10px; color: white ">0</span></button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link py-2 h5 px-4" data-toggle="tab" id="released-tab" href="#released" role="tab">Released<span class="ml-2 rounded" style="background-color: #fbbd08 ; font-size: 12px; padding: 0px 10px 0px 10px; color: white ">0</span></button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link py-2 h5 px-4" data-toggle="tab" id="all-tab" href="#all" role="tab">All<span class="ml-2 rounded" style="background-color: #767676 ; font-size: 12px; padding: 0px 10px 0px 10px; color: white ">0</span></button>
            </li>
        </ul>
    </div>
</div>
<div class="tab-content  ml-3 mr-3 p-3 my-5" id="mytabcontrol">
    <div class="tab-pane active" role="tabpanel" id="forapproval">
        <table id="example" class="display">
            <thead>
                <tr>
                    <th>Pay To</th>
                    <th>Voucher #</th>
                    <th>Check #</th>
                    <th>Payment Method</th>
                    <th>Bank</th>
                    <th>Check Amount</th>
                    <th>Check Date</th>
                    <th>Status</th>
                    <th>Prepared By</th>
                    <th>Encoded Date</th>
                    <th>Action</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Test 1</td>
                    <td>00000000</td>
                    <td> 1111111</td>
                    <td>Online</td>
                    <td>BDO</td>
                    <td>000000</td>
                    <td>2011-04-25</td>
                    <td>Pending</td>
                    <td>Michael Jordan</td>
                    <td>2020-2-2</td>
                    <td>edit delete </td>
                </tr>
            </tbody>
        </table>
    </div>
    <div class="tab-pane " role="tabpanel" id="approved">
        <table id="example1" class="display">
            <thead>
                <tr>
                    <th>Pay To</th>
                    <th>Voucher #</th>
                    <th>Check #</th>
                    <th>Payment Method</th>
                    <th>Bank</th>
                    <th>Check Amount</th>
                    <th>Check Date</th>
                    <th>Status</th>
                    <th>Prepared By</th>
                    <th>Encoded Date</th>
                    <th>Action</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Test 1</td>
                    <td>00000000</td>
                    <td> 1111111</td>
                    <td>Online</td>
                    <td>BDO</td>
                    <td>000000</td>
                    <td>2011-04-25</td>
                    <td>Pending</td>
                    <td>Michael Jordan</td>
                    <td>2020-2-2</td>
                    <td>edit delete </td>
                </tr>
            </tbody>
        </table>
    </div>
    <div class="tab-pane " role="tabpanel" id="posted">
        <table id="example2" class="display">
            <thead>
                <tr>
                    <th>Pay To</th>
                    <th>Voucher #</th>
                    <th>Check #</th>
                    <th>Payment Method</th>
                    <th>Bank</th>
                    <th>Check Amount</th>
                    <th>Check Date</th>
                    <th>Status</th>
                    <th>Prepared By</th>
                    <th>Encoded Date</th>
                    <th>Action</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Test 1</td>
                    <td>00000000</td>
                    <td> 1111111</td>
                    <td>Online</td>
                    <td>BDO</td>
                    <td>000000</td>
                    <td>2011-04-25</td>
                    <td>Pending</td>
                    <td>Michael Jordan</td>
                    <td>2020-2-2</td>
                    <td>edit delete </td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
<script>
    //datatables
    $(document).ready(function () {
        var generalledger = $('#example').DataTable({
            dom: "<'myfilter'f><'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            }
        });
    });
    $(document).ready(function () {
        var generalledger = $('#example1').DataTable({
            dom: "<'myfilter'f><'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            }
        });
    });
    $(document).ready(function () {
        var generalledger = $('#example2').DataTable({
            dom: "<'myfilter'f><'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            }
        });
    });
</script>
<style>
    .nav-tabs .nav-link {
        margin: 0;
    }

        .nav-tabs .nav-link.active:focus {
            background: #2185d0;
            color: #fff;
            border-color: #2185d0;
            border-bottom-color: #2185d0;
        }

        .nav-tabs .nav-link.active {
            background: #2185d0;
            color: #fff;
            border-color: #2185d0;
            border-bottom-color: #2185d0;
        }

    .nav-tabs .nav-link {
        background: #fff;
        border-bottom: 1px solid #c8ced3;
        border-right: 1px solid #c8ced3;
        border-left: 1px solid #c8ced3;
        color: #000;
    }
</style>
```

**Controllers**
```md title="File Location: Controllers/Purchase/CheckPreparation/CheckPreparationController.cs"
public async Task<IActionResult> CheckPreparationListV2()
        {
            return View("~/Views/Purchase/CheckPreparation/CheckPreparationListV2.cshtml");
        }
```

### AddCheckPreparationV2
**Views**
```md title="File Location: Views/Purchase/CheckPreparation/AddCheckPreparationV2.cshtml"
@*
    For more information on enabling MVC for empty projects, visit https://go.microsoft.com/fwlink/?LinkID=397860
*@
@{
}
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3 class="pt-2">
                Prepare Check
            </h3>
        </div>
    </div>
</div>
<div class="card ml-3 mr-3">
    <div class="py-3" style="background-color:rgb(43, 120, 228)"></div>
    <div class=" card-body p-3" style="margin:0; padding: 0;">
        <div class="row mb-3 ">
            <div class="col-lg-4">
                <div style="display:flex; align-items:center;" class="row mb-2">
                    <label class="col-sm-4">Search Voucher:</label>
                    <select class="col-sm-6 form-control mx-2">
                        <option value="1">Account Title</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div style="display:inline-block; align-items:center;" class="mb-2">
                    <div class="" style="display:flex; align-items:center;">
                        <label class="">Pay To:</label>
                    </div>
                    <div class="my-3" style="display:flex; align-items:center;">
                        <div class="my-2"><a href="" data-toggle="modal" data-target="#cancelModal">click to show voucher details</a></div>
                    </div>
                </div>
            </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Payment Mode:</label>
                    <input type="text" class="col-sm-6 form-control mx-2 mb-2"  />
                </div>
                <div style="display:flex; align-items:center;" class="row mb-2">
                    <label class="col-sm-4 ">Bank:</label>
                    <select class="form-control col-sm-6 mx-2">
                        <option value="1">Account Title</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
            </div>
            <div class="col-lg-4">
                <div class="mb-2 row" style="display:flex; align-items:center;">
                    <label class="col-sm-4" style="width:200px">Check Amount:</label>
                    <div class="col-sm-6 mx-2" >P 0.00</div>
                </div>
                <div class="mb-2 row" style="display:flex; align-items:center;">
                    <label class="col-sm-4 ">Check Number:</label>
                    <input  type="text" class="col-sm-6 form-control mx-2" />
                </div>
                <div class="mb-2 row" style="display:flex; align-items:center;">
                    <label class="col-sm-4">Check Date:</label>
                    <input type="date" class="col-sm-6 form-control mx-2"  />
                </div>
            </div>
        </div>
        <div style="display:inline-block; float:right" class="pe-3">
            <div class="card-body text-right">
                <a class="btn btn-brand btn-behance" style="background-color:#21BA45" asp-controller="" asp-action=""><i class="fa fa-print"></i><span>Print Check</span></a>
            </div>
        </div>
    </div>
</div>
<div class="modal fade" id="cancelModal" tabindex="-1" role="dialog" aria-labelledby="cancelModalLabel" aria-hidden="true">
    <div class="modal-dialog" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="cancelModalLabel">Voucher Details</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body p-2">
                <table id="example" class="display">
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>RFP# / PI#</th>
                            <th>Amount</th>
                            <th>WT</th>                            
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td></td>
                            <td</td>
                            <td> </td>
                            <td></td>
                            
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-dismiss="modal">Cancel</button>
            </div>
        </div>
    </div>
</div>
<script>
    //datatables
    $(document).ready(function () {
        var generalledger = $('#example').DataTable({
            dom: "<'myfilter'f><'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            }
        });
    });
</script>
```

**Controllers**
```md title="File Location: Controllers/Purchase/CheckPreparation/CheckPreparationController.cs"
public async Task<IActionResult> AddCheckPreparationV2()
        {
            return View("~/Views/Purchase/CheckPreparation/AddCheckPreparationV2.cshtml");
        }
```

### AddPaymentVoucherV2
**Views**
```md title="File Location: Views/Purchase/PaymentVoucher/AddPaymentVoucherV2.cshtml"
@*
    For more information on enabling MVC for empty projects, visit https://go.microsoft.com/fwlink/?LinkID=397860
*@
@{
}
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3 class="pt-2">
                Payment Voucher
            </h3>
        </div>
    </div>
</div>
<div class="card ml-3 mr-3 mt-3" style="margin-bottom:0;">
    <div class="py-3" style="background-color:rgb(43, 120, 228)"></div>
    <div class=" card-body p-3" style="margin:0; padding: 0;">
        <div class="row mb-3 ">
            <div class="col-lg-6">
                <div style="display:flex; align-items:center;" class="row mb-2">
                    <label class="col-sm-4 ">Bank:</label>
                    <select class="form-control col-sm-6 mx-2">
                        <option value="1">search</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Contact Person: </label>
                </div>
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Address:</label>
                </div>
            </div>
            <div class="col-lg-6">
                <div class="mb-2 row" style="display:flex; align-items:center;">
                    <label class="col-sm-4" style="width:200px">Voucher Date:</label>
                    <input type="date" class="col-sm-6 form-control mx-2" />
                </div>
                <div class="mb-2 row" style="display:flex; align-items:center;">
                    <label class="col-sm-4 ">Payment Method:</label>
                    <select class="form-control col-sm-6 mx-2">
                        <option value="1">payment</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
            </div>
        </div>
        <div>Remarks:</div>
        <textarea placeholder="Type your remarks here" class="my-2 p-1 form-control border-0" row="3"></textarea>
    </div>
</div>
<div class="card ml-3 mr-3">
    <div class="p-2 text-white" style="background-color:rgb(43, 120, 228)">Payable List</div>
    <div class=" card-body p-5" style="margin:0; padding: 0; font-weight:600;">
        <div class="" style="display:flex;align-items:center; justify-content:center">
            <div>
                Nothing to Display
            </div>
        </div>
    </div>
</div>
</div>
```

**Controllers**
```md title="File Location: Controllers/Purchase/CheckPreparation/CheckPreparationController.cs"
public async Task<IActionResult> AddPaymentVoucherV2()
        {
            return View("~/Views/Purchase/PaymentVoucher/AddPaymentVoucherV2.cshtml");
        }
```
