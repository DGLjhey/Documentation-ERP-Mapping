### AddMemoV2
**Views**
```md title="File Location: Views/Sales/Memo/AddMemoV2.cshtml"
@*
    For more information on enabling MVC for empty projects, visit https://go.microsoft.com/fwlink/?LinkID=397860
*@
@{
}
<div class="card mb-0">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h4 class="pt-2">
                Create Memo
            </h4>
        </div>
        <div class="col-md-6 card-body text-right">
            <a class="" asp-controller="Memo" asp-action="Index"><h3><i class="fa fa-times"></i><span class="cui-contrast"></span></h3></a>
        </div>
    </div>
</div>
<div class="card ml-3 mr-3 mt-3 mb-2">
    <div class="py-3" style="background-color:rgb(43, 120, 228)"></div>
    <div class=" card-body p-3" style="margin:0; padding: 0;">
        <div class="row mb-3 ">
            <div class="col-lg-6">
                <div style="display:flex; align-items:center;" class="row mb-2">
                    <label class="col-sm-4 ">Memo Type:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1"></option>
                        <option value="2">Credit</option>
                        <option value="3">Debit</option>
                    </select>
                </div>
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Transaction Type: </label>
                    <select class="form-control col-sm-7 mx-2" id="transaction-type">
                        <option value="yellow" selected>Sales Invoice</option>
                        <option value="red" >Payment Collection</option>
                        <option value="green" >Account Receivable</option>
                    </select>
                </div>
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Sales Invoice No:</label>
                    <input type="text" class="col-sm-7 form-control mx-2" />
                </div>
                <div class="red msg">
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">OR Number:</label>
                    <input type="text" class="col-sm-7 form-control mx-2" />
                </div>
                </div>
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Purpose:</label>
                    <select class="form-control col-sm-7 mx-2">
                        <option value="1"></option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div style="display:flex; align-items:center;" class="mb-2 row">
                    <label class="col-sm-4">Remarks:</label>
                    <textarea placeholder="Type your remarks here" class="my-2 mx-3 p-1 form-control border-0" row="3"></textarea>
                </div>
            </div>
            <div class="col-lg-6">
                <div class="yellow msg">
                    <div class="mb-2 row" id="details" style="display:flex; align-items:center;">
                        <label class="col-sm-4">Details</label>
                    </div>
                    <div class="mb-2 row" id="customer name" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Customer Name</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">SO Number</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Invoice Date</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Invoice Amount</label>
                        <div class="">₱ 0.00</div>

                    </div>
                    </div>
                <div class="red msg">
                    <div class="mb-2 row" id="details" style="display:flex; align-items:center;">
                        <label class="col-sm-4">Details</label>
                    </div>
                    <div class="mb-2 row" id="customer name" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Customer Name</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">OR Number</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Transaction Date</label>
                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Posting Date</label>
                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Mode of Payment</label>
                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Bank</label>
                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Branch</label>
                    </div>
                </div>
                <div class="green msg">
                    <div class="mb-2 row" id="details" style="display:flex; align-items:center;">
                        <label class="col-sm-4">Details</label>
                    </div>
                    <div class="mb-2 row" id="customer name" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Customer Name</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">SO Number</label>
                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Invoice Date</label>

                    </div>
                    <div class="mb-2 row" style="display:flex; align-items:center;">
                        <label class="col-sm-4 ">Invoice Amount</label>
                        <div class="">₱ 0.00</div>
                    </div>
                    </div>
            </div>
        </div>
        
    <div class="card ml-3 mr-3 mb-3">
        <div class="p-2 text-white" style="background-color:rgb(43, 120, 228)">Transaction List</div>
        <div class=" card-body p-5" style="margin:0; padding: 0; font-weight:600;">
            <table id="example" class="display">
                <thead>
                    <tr>
                        <th>Amount</th>
                        <th>Revenue/ Cost Center</th>
                        <th>Debit </th>
                        <th>Credit</th>
                         <th>Action</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        
                    </tr>
                </tbody>
            </table>
            <div class="mt-2">
                    <a class="btn btn-brand text-white me-1" style="background-color:#2185D0" onclick="addRow()"><i class="fa fa-plus"></i><span>Add New Line</span></a>
                <a class="btn btn-brand text-white" style="background-color:#DB2828" onclick="deleteAllRows()"><i class="fa fa-minus"></i><span>Clear All Line</span></a>
            </div>
        </div>
    </div>
    <div class="text-right m-3">
        <a class="btn btn-brand text-white me-2" style="background-color:#21BA45" asp-controller="" asp-action=""><i class="fa fa-floppy-o"></i><span>Saves as Draft</span></a>
        <a class="btn btn-brand text-white me-2" style="background-color:#2185D0" asp-controller="" asp-action=""><i class="fa fa-floppy-o"></i><span>Submit</span></a>
        <a class="btn btn-brand text-white" style="background-color:#DB2828" data-toggle="modal" data-target="#cancelModal" asp-controller="" asp-action=""><i class="fa fa-times"></i><span>Cancel</span></a>
    </div>
        <div class="modal fade" id="cancelModal" tabindex="-1" role="dialog" aria-labelledby="cancelModalLabel" aria-hidden="true">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title" id="cancelModalLabel">Confirmation</h5>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">
                        Are you sure you want to cancel?
                    </div>
                    <div class="modal-footer">
                        <a class="btn btn-brand text-white" href="@Url.Action("Index", "Memo")" style="background-color:#21BA45"><i class="fa fa-check"></i><span>Yes</span></a>
                        <a class="btn btn-brand text-white" data-dismiss="modal" style="background-color:#DB2828"><i class="fa fa-times"></i><span>No</span></a>
                    </div>
                </div>
            </div>
        </div>
</div>
<script>
    $(document).ready(function () {
        var generalledger = $('#example').DataTable({
                dom: "<'myfilter'f > <'mylength'l >",
            ordering: false,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            }
        });
    });

        $(document).ready(function () {
            $("#transaction-type").change(function () {
                $(this).find("option:selected").each(function () {
                    var val = $(this).attr("value");
                    if (val) {
                        $(".msg").not("." + val).hide();
                        $("." + val).show();
                    } else {
                        $(".msg").hide();
                    }
                });
            }).change();
        });



        function addRow() {
            var table = document.getElementById("example");
            var row = table.insertRow(-1);
            var AmountCell = row.insertCell(0);
            var RevenueCell = row.insertCell(1);
            var DebitCell = row.insertCell(2);
            var CreditCell = row.insertCell(3);
            var actionCell = row.insertCell(4);
            var AmountInput = document.createElement("input");
            AmountInput.type = "text";
            AmountInput.className = "form-control form-control-sm";
            AmountCell.appendChild(AmountInput);
            var DebitInput = document.createElement("input");
            DebitInput.type = "number";
            DebitInput.className="form-control form-control-sm";
            DebitCell.appendChild(DebitInput);
            var CreditInput = document.createElement("input");
            CreditInput.type = "number";
            CreditInput.className = "form-control form-control-sm";
            CreditCell.appendChild(CreditInput);
            var RevenueSelect = document.createElement("select");
            RevenueSelect.className = "form-control form-control-sm";
            var Optionone = document.createElement("option");
            Optionone.value = "Process";
            Optionone.text = "Process/Mixing";
            var Optiontwo = document.createElement("option");
            Optiontwo.value = "Warehouse";
            Optiontwo.text = "FG Warehouse";
            var Optionthree = document.createElement("option");
            Optionthree.value = "Inspection";
            Optionthree.text = "QA Inspection";
            RevenueSelect.appendChild(Optionone);
            RevenueSelect.appendChild(Optiontwo);
            RevenueSelect.appendChild(Optionthree);
            RevenueCell.appendChild(RevenueSelect);
            var deleteButton = document.createElement("button");
            deleteButton.type = "button";
            deleteButton.className="btn btn-brand text-white";
            deleteButton.style.backgroundColor="#DB2828";
            deleteButton.textContent = "Delete";
            deleteButton.onclick = function () {
                deleteRow(this);
            };
            actionCell.appendChild(deleteButton);
        }

        function deleteRow(button) {
            var table = document.getElementById("example");
            var row = button.parentNode.parentNode;
            table.deleteRow(row.rowIndex);
        }

        function deleteAllRows() {
            var table = document.getElementById("example");
            var rowCount = table.rows.length;
            for (var i = rowCount - 1; i > 0; i--) {
                table.deleteRow(i);
            }
        }
    </script>

```

**Controllers**
```md title="File Location: Controllers/Sales/Memo/MemoController.cs"
 public async Task<IActionResult> AddMemoV2()
        {
            return View("~/Views/Sales/Memo/AddMemoV2.cshtml");
        }
```
