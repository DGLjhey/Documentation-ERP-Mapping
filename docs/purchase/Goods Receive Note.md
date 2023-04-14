### EditGoodsReceiveNoteV2
**Views**
```md title="File Location: Views/Purchase/GoodsReceiveNote/EditGoodsReceiveNoteV2.cshtml"
@{
    ViewData["Title"] = "EditGoodsReceiveNoteV2";
    Layout = "~/Views/Shared/_Layout.cshtml";
}

@*========== Header of the Page ==========*@
<div class="card">
    <div class="row ml-2 mr-2 p-4">
        <div class="col-md-6 col-sm-6 col-6 p-0">
            <h3 class="">
                Edit Goods Receipt Note
            </h3>
        </div>
        <div class="col-md-6 col-sm-6 col-6 -0 text-right">
            <a href="/GoodsReceiveNote/"><h3><i class="fa fa-times"></i><span class="cui-contrast"></span></h3></a>
        </div>
    </div>
</div>
@*========== Body of the Page ==========*@
<div class="container-fluid">
    <div class="row justify-content-center mt-4">
        <div class="col-lg-12 col-md-8 col-sm-10">
            <div class="card">
                <div class="card-body">
                    @*========== First Card ==========*@
                    <div class="card mx-auto w-75">
                        <div class="bg-primary col-12 py-2 pl-3">
                            <h5>Details</h5>
                        </div>
                        <div class="card-body">
                            <div class="row">
                                <div class="col-12">
                                    <div class="row">
                                        <div class="col-12">
                                            @*========== First Card - Supplier ==========*@
                                            <div class="row justify-content-center">
                                                <div class="col-lg-3 col-md-3 col-sm-12 mr-5">
                                                    <label class="float-lg-right font-weight-bold">Supplier:</label>
                                                </div>
                                                <div class="col-lg-4 col-md-4 col-sm-12">
                                                    <p class="font-weight-bold">PHILKO SILICATE CORPORATION</p>
                                                </div>
                                            </div>
                                        </div>
                                        @*========== First Card - GRN No. ==========*@
                                        <div class="col-12">
                                            <div class="row justify-content-center">
                                                <div class="col-lg-3 col-md-3 col-sm-12 mr-5">
                                                    <label class="float-lg-right float-sm-none font-weight-bold">GRN No.:</label>
                                                </div>
                                                <div class="col-lg-4 col-md-4 col-sm-12">
                                                    <p class="font-weight-bold">PMCGRN-0000002363</p>
                                                </div>
                                            </div>
                                        </div>
                                        @*========== First Card - PO No. ==========*@
                                        <div class="col-12">
                                            <div class="row justify-content-center">
                                                <div class="col-lg-3 col-md-3 col-sm-12 mr-5">
                                                    <label class="float-lg-right float-sm-none font-weight-bold">PO No.:</label>
                                                </div>
                                                <div class="col-lg-4 col-md-4 col-sm-12">
                                                    <p class="font-weight-bold">PMCPO-0000000149</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    @*========== Second Card ==========*@
                    <div class="card mx-auto w-75">
                        <div class="card-body">
                            <div class="row">
                                @*========== Second Card - Text Display on the Upper Left ==========*@
                                <div class="col-12 mb-3">
                                    <p id="textInput" class="font-weight-bold">Please input <span id="change" class="text-danger">Delivery Receipt Number</span></p>
                                </div>
                                <div class="col-12">
                                    <div class="row">
                                        <div class="col-lg-6 col-md-12 col-sm-12">
                                            <div class="row">
                                                @*========== Second Card - Input for DR No. ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-lg-4 col-md-4 col-sm-12">
                                                            <label class="font-weight-bold">DR No.<span class="text-danger">*</span>:</label>
                                                        </div>
                                                        <div class="col-lg-8 col-md-8 col-sm-12">
                                                            <input id="drNo" type="text" class="form-control input-box" />
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Second Card - Input for Driver Name ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-lg-4 col-md-4 col-sm-12">
                                                            <label class="font-weight-bold">Driver Name<span class="text-danger">*</span>:</label>
                                                        </div>
                                                        <div class="col-lg-8 col-md-8 col-sm-12">
                                                            <input id="driverName" type="text" class="form-control input-box" />
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Second Card - Input for Plate Number ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-lg-4 col-md-4 col-sm-12">
                                                            <label class="font-weight-bold">Plate Number<span class="text-danger">*</span>:</label>
                                                        </div>
                                                        <div class="col-lg-8 col-md-8 col-sm-12">
                                                            <input id="plateNumber" type="text" class="form-control input-box" />
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Second Card - Input for Remarks ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-12">
                                                            <label class="font-weight-bold">Remarks:</label>
                                                        </div>
                                                        <div class="col-12">
                                                            <textarea class="form-control border-0 shadow-none" placeholder="Type your remarks here"></textarea>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-lg-6 col-md-12 col-sm-12">
                                            <div class="row">
                                                @*========== Second Card - Input for Inbound ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-lg-4 col-md-4 col-sm-12">
                                                            <label class="font-weight-bold">Inbound<span class="text-danger">*</span>:</label>
                                                        </div>
                                                        <div class="col-lg-8 col-md-8 col-sm-12">
                                                            <input id="inbound" type="number" class="form-control input-box" placeholder="0" />
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Second Card - Input for Outbound ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-lg-4 col-md-4 col-sm-12">
                                                            <label class="font-weight-bold">Outbound:</label>
                                                        </div>
                                                        <div class="col-lg-8 col-md-8 col-sm-12">
                                                            <input type="text" class="form-control" placeholder="0" disabled />
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Second Card - Input for Weight ==========*@
                                                <div class="col-12 mb-2">
                                                    <div class="row">
                                                        <div class="col-lg-4 col-md-4 col-sm-12">
                                                            <label class="font-weight-bold">Weight:</label>
                                                        </div>
                                                        <div class="col-lg-8 col-md-8 col-sm-12">
                                                            <p class="font-weight-bold"><span>0</span> Kg</p>
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Second Card - Submit Button ==========*@
                                                <div class="col-12 mt-5">
                                                    <div class="row">
                                                        <div class="col-4">
                                                        </div>
                                                        <div class="col-8">
                                                            @*========== Submit Button Trigger Modal ==========*@
                                                            <button id="submit-btn" type="button" class="btn btn-primary w-100" data-toggle="modal" data-target="#submitModal" disabled><i class="fa fa-floppy-o pr-2"></i> Submit</button>
                                                        </div>
                                                    </div>
                                                </div>
                                                @*========== Submit Button Modal ==========*@
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
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    // get all input elements
    const drNoInput = document.getElementById("drNo");
    const driverNameInput = document.getElementById("driverName");
    const plateNoInput = document.getElementById("plateNumber");
    const inboundInput = document.getElementById("inbound");
    const changeSpan = document.getElementById('change');
    const textInputSpan = document.getElementById('textInput');

    // function to change the text content
    $(".input-box").change(function () {
        var drNo = $("#drNo").val();
        var driverName = $("#driverName").val();
        var plateNo = $("#plateNumber").val();
        var inbound = $("#inbound").val();
        
        //condtion for the text content
        if (drNo != "" && driverName != "" && plateNo != "" && inbound != 0) {
            $("#textInput").hide();
        } else {
            $("#textInput").show()
            if (drNoInput.value == '') {
                changeSpan.textContent = 'Delivery Receipt Number';
            } else if (driverNameInput.value == '') {
                changeSpan.textContent = 'Driver Name';
            } else if (plateNoInput.value == '') {
                changeSpan.textContent = 'Plate Number';
            } else if (inboundInput.value == '') {
                changeSpan.textContent = 'Inbound Weight';
            }
        }
    });

    // get the submit button element
    const submitBtn = document.getElementById("submit-btn");

    // add event listeners to input elements to check if they have values
    drNoInput.addEventListener("input", toggleSubmitBtn);
    driverNameInput.addEventListener("input", toggleSubmitBtn);
    plateNoInput.addEventListener("input", toggleSubmitBtn);
    inboundInput.addEventListener("input", toggleSubmitBtn);

    // function to toggle the submit button
    function toggleSubmitBtn() {
        // check if all input elements have values
        if (
            drNoInput.value !== "" &&
            driverNameInput.value !== "" &&
            plateNoInput.value !== "" &&
            inboundInput.value !== ""
        ) {
            // enable the submit button
            submitBtn.disabled = false;
        } else {
            // disable the submit button
            submitBtn.disabled = true;
        }
    }
</script>
```

**Controllers**
```md title="File Location: Controllers/Purchase/GoodsReceiveNote/GoodsReceiveNoteController.cs"public IActionResult EditGoodsReceiveNoteV2()
        {
            return View("~/Views/Purchase/GoodsReceiveNote/EditGoodsReceiveNoteV2.cshtml");
        }
Code Here
```