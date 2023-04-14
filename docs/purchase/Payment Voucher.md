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
```md title="File Location: Controllers/Purchase/PaymentVoucher/PaymentVoucherController.cs"
public async Task<IActionResult> AddPaymentVoucherV2()
        {
            return View("~/Views/Purchase/PaymentVoucher/AddPaymentVoucherV2.cshtml");
        }
```
