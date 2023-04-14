### AllStockOnHAndV2
**Views**
```md title="File Location: Views/Inventory/AllStockOnHand/AllStockOnHAndV2.cshtml"
@{
    ViewData["Title"] = "AllStockOnHandV2";
    //Layout = "/~Views/Shared/_Layout.cshtml";
}

    <div class="card">
        <div class="ml-2">
            <div class="card-body">
                <h4>Stock On Hand</h4>
            </div>
        </div>
    </div>

    <div class="card m-4 p-4">
        <div class="row">

            @*First Section*@
            <div class="col-lg-2 col-md-12 col-sm-12">
                <p><strong>Filter By:</strong></p>
            </div>
            @*End First Section*@

            @*Second Section*@
            <div class="col-lg-4 col-md-12 col-sm-12">
                <div class="row mb-2 ">
                    <div class="col">
                        <label><strong>Plant</strong></label>
                    </div>
                    <div class="col">
                        <div class="">
                            <select class="form-control" style="width: 20rem;">
                                <option selected>All Plants</option>
                                <option value="1">Canlubang</option>
                                <option value="2">Valenzuela</option>
                                <option value="3">Laguna</option>
                                <option value="3">IPIC</option>
                            </select>
                        </div>
                    </div>
                </div>

                <div class="row mb-2">
                    <div class="col">
                        <label><strong>Warehouse</strong></label>
                    </div>
                    <div class="col">
                        <div class="">
                            <select class="form-control" style="width: 20rem;">
                                <option selected>All Warehouse</option>
                                <option value="1">Canlubang-Building 4</option>
                                <option value="2">Canlubang-Building 5</option>
                                <option value="3">Canlubang-HALA</option>
                                <option value="4">Valenzuela-Building 1</option>
                                <option value="5">Valenzuela-Building 2</option>
                                <option value="6">Valenzuela-Building 3</option>
                                <option value="7">Valenzuela-Building 4</option>
                                <option value="8">Valenzuela-Building 5</option>
                                <option value="9">Canlubang-Building 06 & 07 (In Between)</option>
                                <option value="10">Canlubang-Building 04 & 05 (In Between)</option>
                                <option value="11">Canlubang-Building 05 & 06 (In Between)</option>
                                <option value="12">Canlubang-Building 09 & 10 (In Between)</option>
                                <option value="13">Canlubang-Building 08 & 09 (In Between)</option>
                                <option value="14">Valenzuela-Tank Farm</option>
                                <option value="15">Canlubang-Canlubang RMPM</option>
                                <option value="16">Canlubang-Building 12</option>
                                <option value="17">Canlubang-Building 13</option>
                                <option value="18">Canlubang-Building 01 & 02 (In Between)</option>
                                <option value="19">Valenzuela-POWDER WAREHOUSE</option>
                                <option value="20">Valenzuela-Building 6</option>
                                <option value="21">IPIC-IPIC-Building 6</option>
                                <option value="22">IPIC-IPIC-Building 5</option>
                            </select>
                        </div>
                    </div>
                </div>
            </div>
            @*End Second Section*@

            @*Third Section*@
            <div class="col-lg-4 col-md-12 col-sm-12">
                <div class="row mb-2">
                    <div class="col">
                        <label><strong>Item Group</strong></label>
                    </div>
                    <div class="col">
                        <div class="">
                            <select class="form-control" style="width: 20rem;">
                                <option selected>All Item Group</option>
                                <option value="1">Item 1</option>
                                <option value="2">Item 2</option>
                                <option value="3">Item 3</option>
                                <option value="4">Item 4</option>
                                <option value="5">Item 5</option>
                            </select>
                        </div>
                    </div>
                </div>

                <div class="row mb-2">
                    <div class="col">
                        <label><strong>Material Type</strong></label>
                    </div>
                    <div class="col">
                        <div class="">
                            <select class="form-control" style="width: 20rem;">
                                <option selected>All Material Type</option>
                                <option value="1">Item 1</option>
                                <option value="2">Item 2</option>
                                <option value="3">Item 3</option>
                                <option value="4">Item 4</option>
                                <option value="5">Item 5</option>
                            </select>
                        </div>
                    </div>
                </div>

                <div class="row mb-2">
                    <div class="col">
                        <label><strong>Category</strong></label>
                    </div>
                    <div class="col">
                        <div class="">
                            <select class="form-control" style="width: 20rem;">
                                <option selected>All Category</option>
                                <option value="1">Item 1</option>
                                <option value="2">Item 2</option>
                                <option value="3">Item 3</option>
                                <option value="4">Item 4</option>
                                <option value="5">Item 5</option>
                            </select>
                        </div>
                    </div>
                </div>

                <div class="row mb-2">
                    <div class="col">
                        <label><strong>Subcategory</strong></label>
                    </div>
                    <div class="col">
                        <div class="">
                            <select class="form-control" style="width: 20rem;">
                                <option selected>All Sub - Category</option>
                                <option value="1">Item 1</option>
                                <option value="2">Item 2</option>
                                <option value="3">Item 3</option>
                                <option value="4">Item 4</option>
                                <option value="5">Item 5</option>
                            </select>
                        </div>
                    </div>
                </div>
            </div>
            @*End of Third Section*@

            @*Forth Section*@
            <div class="row col-2">
                <div class="col d-flex flex-column">
                    <button class="btn btn-success mb-2 disabled" style="width:7rem;"><i class="fa fa-print"></i> Print</button>
                    <button class="btn btn-primary mb-2" style="width:7rem;"><i class="fa fa-filter"></i> Filter</button>
                    <button class="btn btn-warning mb-2 disabled" style="width:7rem;"><i class="fa fa-file"></i> Export</button>
                </div>
            </div>
            @*End of Fourth Section*@
        </div>
        @*End of row*@

        <hr>

        @*Start of Search Bar*@
        <div class="ml-auto mb-2">
            <form class="form-inline">
                <input class="form-control" type="search" placeholder="Search" aria-label="Search" style="width:400px;">
            </form>
        </div>
        @*End of Search Bar*@

        @*Table section*@
        <div class="row">
            <div class="col-12 table-responsive">
                <table id="Table" class="table table-striped table-bordered">
                    <thead>
                        <tr>
                            <th>Item Code</th>
                            <th>Item Name</th>
                            <th>Base Unit</th>
                            <th>Warehouse</th>
                            <th>Material Type</th>
                            <th>Category</th>
                            <th>Sub Category</th>
                            <th>On Hand</th>
                            <th>Reserved</th>
                            <th>Balance</th>
                        </tr>
                    </thead>
                    <tbody>
                        @*
                        <tr>
                            <td colspan="10" class="text-center">There is no data to display</td>
                        </tr>*@
                    </tbody>
                </table>
            </div>
        </div>
        @*End of Table section*@

        @*Dropdown Number section*@
        <div class="dropdown mt-3">
            <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                10
            </button>
            <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                <a class="dropdown-item" href="#">10</a>
                <a class="dropdown-item" href="#">25</a>
                <a class="dropdown-item" href="#">30</a>
                <a class="dropdown-item" href="#">50</a>
            </div>
        </div>
        @*End Dropdown Number section*@
    </div>

@*Script that includes Filter/Search Bar*@
@*
<script>
    $(document).ready(function () {

        $('#Table').DataTable({
            dom: "<'myfilter'f><'mylength'l>tip",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
        });
    });
</script>*@

@*Script that doesn't includes Filter/Search Bar,length*@
<script>
    $(document).ready(function () {

        $('#Table').DataTable({
            dom: "",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
        });
    });
</script>
```

**Controllers**
```md title="File Location: Controllers/Inventory/AllStockOnHand/AllStockOnHAndController.cs"
public async Task<IActionResult> AllStockOnHandV2()
        {
            return View("~/Views/Inventory/AllStockOnHand/AllStockOnHandV2.cshtml");
        }
```
