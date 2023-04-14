### AddDeliveryAdjustmentV2
**Views**
```md title="File Location: Views/Sales/DeliveryAdjustment/AddDeliveryAdjustmentV2.cshtml"
@{
    ViewData["Title"] = "AddSalesReturnV3";
    Layout = "~/Views/Shared/_Layout.cshtml";
}

<div class="card m-0">
    <div class="row mx-2">
        <div class="col-6 card-body">
            <h4>Create Delivery Receipt Adjustment</h4>
        </div>
        <div class="col-6 card-body text-right">
            <h3><a href="/DeliveryAdjustment"><i class="fa fa-times"></i></a></h3>
        </div>
    </div>
</div>

<div class="container-fluid mt-3">
    <div class="card">
        <div class="container p-4">
            <div class="row row-cols-2">
                <div class="col-6">
                    <div class="row align-items-center pb-2">
                        <div class="col-4">
                            <p class="mb-0 font-weight-bold">DR No.</p>
                        </div>
                        <div class="col-8">
                            <div width="1500px" class="ui search">
                                <div class="ui fluid icon input">
                                    <input placeholder="Search by delivery receipt or customer" type="text" tabindex="0" class="prompt" autocomplete="off" value="">
                                    <i aria-hidden="true" class="search icon"></i>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="row align-items-center pb-2">
                        <div class="col-4 ">
                            <p class="mb-0 font-weight-bold">SO No.</p>
                        </div>
                        <div class="col-8">
                            <label></label>
                        </div>
                    </div>
                </div>
                <div class="col-6">
                    <div class="row align-items-center pt-2 pb-3">
                        <div class="col-4 ">
                            <p class="mb-0 font-weight-bold">SI No.</p>
                        </div>
                        <div class="col-8">
                            <label></label>
                        </div>
                    </div>

                    <div class="row align-items-center pb-2">
                        <div class="col-4 ">
                            <p class="mb-0 font-weight-bold">Delivery Date</p>
                        </div>
                        <div class="col-8">
                            <div>
                                <input class="form form-control" type="date" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="pt-4 ">
                <table class="table table-striped table-bordered table-sm display nowrap" id="myTable" cellspacing="0" width="100%">
                    <thead>
                        <tr>
                            <th class="col-2">Item Code</th>
                            <th class="col-2">Item Name</th>
                            <th class="col-1">Quantity</th>
                            <th class="col-1">UOM</th>
                            <th class="col-2">Adjustment</th>
                            <th class="col-2">Reason</th>
                            <th class="col-2">Warehouse From</th>
                            <th class="col-2">Location From</th>
                        </tr>
                    </thead>
                    <tbody>
                    </tbody>
                </table>
            </div>

            <div class="container px-0 pt-4">
                <div class="mb-2 font-weight-bold">
                    <p>Remarks: </p>
                </div>
                <div>
                    <textarea placeholder="Type your remarks here..." class="form form-control"></textarea>
                </div>
                <div class="pt-3 float-right">
                    <button type="button" class="btn btn-success disabled"><i class="save icon"></i>Save as Draft</button>
                    <button type="button" class="btn btn-primary disabled"><i class="save icon"></i>Submit</button>
                    <button type="button" class="btn btn-danger " data-toggle="modal" data-target="#cancelModal"><i class="cancel icon"></i>Cancel</button>
                    <div class="modal fade" id="cancelModal" data-backdrop="static" data-keyboard="false" tabindex="-1" role="dialog" aria-labelledby="cancelModalLabel" aria-hidden="true">
                        <div class="modal-dialog " role="document">
                            <div class="modal-content">
                                <div class="modal-header">
                                    <h1 class="modal-title fs-5" id="cancelModalLabel">Confirmation</h1>
                                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                                        <span aria-hidden="true">&times;</span>
                                    </button>
                                </div>
                                <div class="modal-body">
                                    <h4>Are you sure you want to cancel?</h4>
                                </div>
                                <div class="modal-footer">
                                    <a href="@Url.Action("Index", "DeliveryAdjustment")"><button type="button" class="btn btn-success"><i class="checkmark icon"></i>Yes</button></a>
                                    <button class="btn btn-danger" data-dismiss="modal"><i class="cancel icon"></i>No</button>
                                </div>
                            </div>
                        </div>
                    </div>



                </div>
            </div>
        </div>

        <script>
            $(document).ready(function () {
                var table = $('#myTable').DataTable();
                
            });
        </script>
```

**Controllers**
```md title="File Location: Controllers/Sales/DeliveryAdjusment/DeliveryAdjustmentController.cs"
 public IActionResult AddDeliveryAdjustmentV2()
        {
            return View("~/Views/Sales/DeliveryAdjustment/AddDeliveryAdjustmentV2.cshtml");
        }
```
