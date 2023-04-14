### GeneralLedgerV2
**Views**
```md title="File Location: Views/Accounting/GeneralLedger/GeneralLedgerV2.cshtml"
@*
    For more information on enabling MVC for empty projects, visit https://go.microsoft.com/fwlink/?LinkID=397860

*@
@{
    Layout = "~/Views/Shared/_Layout.cshtml";
}
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3 class="pt-2">
                General Ledger
            </h3>

        </div>
        <div class="col-md-6 card-body text-right">
            <a class="btn btn-brand btn-behance" asp-controller="GeneralLedger" asp-action="CloseGeneralLedgerV2"><i class="fa fa-plus-square"></i><span>Close General Ledger</span></a>
        </div>
    </div>
</div>
<div class="card ml-3 mr-3">
    <div class=" card-body" style="margin:0; padding: 0;">
        <ul class="nav nav-tabs" style="    flex-wrap: nowrap;overflow-x: auto; overflow-y:hidden">
            <li class="nav-item active" role="tablist">
                <button class="nav-link active h5 py-3 px-5" data-toggle="tab" id="home-tab" href="#home" role="tab">Home<span class="ml-2 rounded" style="background-color: #2185d0 ; font-size: 12px; padding: 0px 10px 0px 10px; color: white ">0</span></button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link py-3 h5 px-5" data-toggle="tab" id="home-tab" href="#profile" role="tab">Close<span class="ml-2 rounded" style="background-color: #DB2828 ; font-size: 12px; padding: 0px 10px 0px 10px; color: white ">0</span></button>
            </li>
            <li class="nav-item" role="presentation">
                <button class="nav-link py-3 h5 px-5" data-toggle="tab" id="home-tab" href="#blog" role="tab">All<span class="ml-2 rounded" style="background-color: #767676 ; font-size: 12px; padding: 0px 10px 0px 10px; color: white ">0</span></button>
            </li>
        </ul>
    </div>
</div>
<div class="tab-content  ml-3 mr-3 p-3 my-5" id="mytabcontrol">
    <div class="tab-pane active" role="tabpanel" id="home">
                   <div class="row mb-3">
                <div class="col-lg-4">
                    <div style="display:flex; align-items:center" class="row mb-3">
                        <label class="col-4">Year: </label>
                    <input type="date" class=" form-control col-sm-7 mx-2" />
                    </div>
                </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Period: </label>
                    <input type="text" class="form-control col-sm-7 mx-2" placeholder="Search" />
                </div>
            </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Period: </label>
                    <input type="text" class="form-control col-sm-7 mx-2" name="daterange" value="03/28/2023 - 03/29/2023" />
                </div>
            </div>
            </div>
            <div class="mt-1 ml-3 mb-4">Other filters: </div>
            <div class="row mb-3">
                <div class="col-lg-6">
                    <div class="row mb-3"  style="display:flex; align-items:center">
                    <label class="col-sm-4">AccountName:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Account Title</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                    </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Account Code:</label>
                    <div class="col-sm-7 mx-2">
                        <div class="row">
                            <input type="text" class=" col-5 form-control" placeholder="From" />
                            <div class="col-auto px-1">-</div>
                            <input type="text" class="col-5 form-control" placeholder="To" />
                        </div>
                    </div>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Reference:</label>
                    <div class="col-sm-7 mx-2">
                        <div class="row">
                            <input type="text" class=" col-5 form-control" placeholder="From" />
                            <div class="col-auto px-1">-</div>
                            <input type="text" class="col-5 form-control" placeholder="To" />
                        </div>
                    </div>
                </div>
                </div>
            <div class="col-lg-6">
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Journal:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Journal</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Customer/Supplier/Employee:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Customer/Supplier/Employee</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Internal Control No:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Internal Control</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
            </div>
            </div>
            
        <div class="my-4 row" style="display:flex; align-items:center; justify-content:flex-end;">
            <a class="btn btn-brand text-white mx-1 col-auto my-2" style="background-color:#21BA45;"><i class="fa fa-solid fa-filter"></i><span>Filter</span></a>
            <a class="btn btn-brand mx-1 text-white col-auto my-2" style="background-color:#DB2828;"><i class="fa fa-solid fa-filter"></i><span>Clear Filter</span></a>
            <a class="btn btn-brand mx-1 text-white col-auto my-2" style="background-color:#2185D0;"><i class="fa fa-solid fa-file"></i><span>Export</span></a>
        </div>
        <div class="row">
            <div class="col-12" style="overflow-x:auto;">
                <table id="example" class="display">
                    <thead>
                        <tr>
                            <th>Date</th>
                            <th>Reference</th>
                            <th>Transaction Type</th>
                            <th>Explanation</th>
                        </tr>
                    </thead>
                    <tbody>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
    <div class="tab-pane " role="tabpanel" id="profile">
            <div class="row mb-3">
                <div class="col-lg-4">
                    <div style="display:flex; align-items:center" class="row mb-3">
                        <label class="col-4">Year: </label>
                    <input type="date" class=" form-control col-sm-7 mx-2" />
                    </div>
                </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Period: </label>
                    <input type="text" class="form-control col-sm-7 mx-2" placeholder="Search" />
                </div>
            </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Period: </label>
                    <input type="text" class="form-control col-sm-7 mx-2" name="daterange" value="03/28/2023 - 03/29/2023" />
                </div>
            </div>
            </div>
            <div class="mt-1 ml-3 mb-4">Other filters: </div>
            <div class="row mb-3">
                <div class="col-lg-6">
                    <div class="row mb-3"  style="display:flex; align-items:center">
                    <label class="col-sm-4">AccountName:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Account Title</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                    </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Account Code:</label>
                    <div class="col-sm-7 mx-2">
                        <div class="row">
                            <input type="text" class=" col-5 form-control" placeholder="From" />
                            <div class="col-auto px-1">-</div>
                            <input type="text" class="col-5 form-control" placeholder="To" />
                        </div>
                    </div>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Reference:</label>
                    <div class="col-sm-7 mx-2">
                        <div class="row">
                            <input type="text" class=" col-5 form-control" placeholder="From" />
                            <div class="col-auto px-1">-</div>
                            <input type="text" class="col-5 form-control" placeholder="To" />
                        </div>
                    </div>
                </div>
                </div>
            <div class="col-lg-6">
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Journal:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Journal</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Customer/Supplier/Employee:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Customer/Supplier/Employee</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Internal Control No:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Internal Control</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
            </div>
            </div>
            
        <div class="my-4 row" style="display:flex; align-items:center; justify-content:flex-end;">
            <a class="btn btn-brand text-white mx-1 col-auto my-2" style="background-color:#21BA45;"><i class="fa fa-solid fa-filter"></i><span>Filter</span></a>
            <a class="btn btn-brand mx-1 text-white col-auto my-2" style="background-color:#DB2828;"><i class="fa fa-solid fa-filter"></i><span>Clear Filter</span></a>
            <a class="btn btn-brand mx-1 text-white col-auto my-2" style="background-color:#2185D0;"><i class="fa fa-solid fa-file"></i><span>Export</span></a>
        </div>
        <div class="row">
            <div class="col-12" style="overflow-x:auto;">
                <table id="example1" class="display">
                    <thead>
                        <tr>
                            <th>Date</th>
                            <th>Reference</th>
                            <th>Transaction Type</th>
                            <th>Explanation</th>
                        </tr>
                    </thead>
                    <tbody>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
    <div class="tab-pane " role="tabpanel" id="blog">
        <div class="row mb-3">
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Year: </label>
                    <input type="date" class=" form-control col-sm-7 mx-2" />
                </div>
            </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Period: </label>
                    <input type="text" class="form-control col-sm-7 mx-2" placeholder="Search" />
                </div>
            </div>
            <div class="col-lg-4">
                <div style="display:flex; align-items:center" class="row mb-3">
                    <label class="col-4">Period: </label>
                    <input type="text" class="form-control col-sm-7 mx-2" name="daterange" value="03/28/2023 - 03/29/2023" />
                </div>
            </div>
        </div>
        <div class="mt-1 ml-3 mb-4">Other filters: </div>
        <div class="row mb-3">
            <div class="col-lg-6">
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">AccountName:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Account Title</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Account Code:</label>
                    <div class="col-sm-7 mx-2">
                        <div class="row">
                            <input type="text" class=" col-5 form-control" placeholder="From" />
                            <div class="col-auto px-1">-</div>
                            <input type="text" class="col-5 form-control" placeholder="To" />
                        </div>
                    </div>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Reference:</label>
                    <div class="col-sm-7 mx-2">
                        <div class="row">
                            <input type="text" class=" col-5 form-control" placeholder="From" />
                            <div class="col-auto px-1">-</div>
                            <input type="text" class="col-5 form-control" placeholder="To" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-lg-6">
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Journal:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Journal</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Customer/Supplier/Employee:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Customer/Supplier/Employee</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="row mb-3" style="display:flex; align-items:center">
                    <label class="col-sm-4">Internal Control No:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1">Internal Control</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
            </div>
        </div>

        <div class="my-4 row" style="display:flex; align-items:center; justify-content:flex-end;">
            <a class="btn btn-brand text-white mx-1 col-auto my-2" style="background-color:#21BA45;"><i class="fa fa-solid fa-filter"></i><span>Filter</span></a>
            <a class="btn btn-brand mx-1 text-white col-auto my-2" style="background-color:#DB2828;"><i class="fa fa-solid fa-filter"></i><span>Clear Filter</span></a>
            <a class="btn btn-brand mx-1 text-white col-auto my-2" style="background-color:#2185D0;"><i class="fa fa-solid fa-file"></i><span>Export</span></a>
        </div>
        <div class="row">
            <div class="col-12" style="overflow-x:auto;">
                <table id="example2" class="display">
                    <thead>
                        <tr>
                            <th>Date</th>
                            <th>Reference</th>
                            <th>Transaction Type</th>
                            <th>Explanation</th>
                        </tr>
                    </thead>
                    <tbody>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</div>
<div class="py-2"></div>
<script>
    //datatables
    $(document).ready(function () {
        var generalledger = $('#example').DataTable({
            dom: "<'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os',
            }
        });
    });
    $(document).ready(function () {
        var generalledger = $('#example1').DataTable({
            dom: "<'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            } 
        });
    });
     $(document).ready(function () {
        var generalledger = $('#example2').DataTable({
            dom: "<'mylength'l>",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            }
        });
    });
</script>
<style>
    .nav-tabs .nav-link{
        margin:0;
    }
    .nav-tabs .nav-link.active:focus {
        background: #2185d0 ;
        color:#fff;
            border-color: #2185d0 ;
        border-bottom-color: #2185d0 ;
    }
    .nav-tabs .nav-link.active {
        background: #2185d0 ;
        color:#fff;
            border-color: #2185d0;
            border-bottom-color: #2185d0;
    }
    .nav-tabs .nav-link{
        background:#fff;
        border-bottom: 1px solid #c8ced3;
                border-right: 1px solid #c8ced3;

                        border-left: 1px solid #c8ced3;

        color:#000;
    }

    .card-body .nav-tabs{
        border:0;
    }
    .card-body{
        border:0;
    }
   
</style>
```

**Controllers**
```md title="File Location: Controllers/Accounting/GeneralLedger/GeneralLedgerController.cs"
public async Task<IActionResult> GeneralLedgerV2()
        {
            return View("~/Views/Accounting/GeneralLedger/GeneralLedgerV2.cshtml");
        }
```
