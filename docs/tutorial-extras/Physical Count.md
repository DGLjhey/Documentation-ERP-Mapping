### PhysicalCountV2
**Views**
```md title="File Location: Views/Inventory/PhysicalCount/PhysicalCountV2.cshtml"

@{
    ViewData["Title"] = "PhysicalCount";
    Layout = "~/Views/Shared/_Layout.cshtml";
}
<div class="card">
    <div class="m-3">
        <div class="row">
            <div class="col-sm-6">
                <h4 class="ml-2 mt-2">Physical Count</h4>
            </div>
            <div class="col-sm-6 text-right">
                <button class="btn btn-primary" data-toggle="modal" data-target="#uploadModal"><i class="fa fa-upload"></i> Upload Physical Count</button>
                <div class="modal fade" id="uploadModal" tabindex="-1" role="dialog" aria-labelledby="uploadModalLabel" aria-hidden="true">
                    <div class="modal-dialog modal-lg" role="document">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h5 class="modal-title" id="uploadModalLabel">Upload Physical Count Excel File</h5>
                                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                                    <span aria-hidden="true">&times;</span>
                                </button>
                            </div>
                            <div class="modal-body text-center">
                                You can also upload your Physical Count Excel, just import the file
                                <form>
                                    <input class="text-center" type="file" name="file">
                                </form>
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                                <button type="submit" class="btn btn-primary">Upload</button>

                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
</div>

<!-- Navigation Tabs -->
<div class="card mx-5">
    <ul class="nav nav-pills flex-column flex-sm-row" id="ex1" role="tablist">
        <li class="nav-item tabName" role="presentation">
            <a class="nav-link active text-dark"
               id="ex1-tab-1"
               data-toggle="tab"
               href="#ex1-tabs-1"
               role="tab"
               aria-controls="ex1-tabs-1"
               aria-selected="true">General System Count</a>
        </li>
        <li class="nav-item tabName" role="presentation">
            <a class="nav-link  text-dark"
               id="ex1-tab-2"
               data-toggle="tab"
               href="#ex1-tabs-2"
               role="tab"
               aria-controls="ex1-tabs-2"
               aria-selected="false">
                Ongoing System Count
                <span class="pl-3 pr-3 bg-warning ml-2 rounded">0</span>
            </a>
        </li>
        <li class="nav-item tabName" role="presentation">
            <a class="nav-link  text-dark"
               id="ex1-tab-3"
               data-toggle="tab"
               href="#ex1-tabs-3"
               role="tab"
               aria-controls="ex1-tabs-3"
               aria-selected="false">
                For Approval
                <span class="pl-3 pr-3 bg-success ml-2 rounded">0</span>
            </a>
        </li>
        <li class="nav-item tabName" role="presentation">
            <a class="nav-link  text-dark"
               id="ex1-tab-4"
               data-toggle="tab"
               href="#ex1-tabs-4"
               role="tab"
               aria-controls="ex1-tabs-4"
               aria-selected="false">
                Approved
                <span class="pl-3 pr-3 bg-primary ml-2 rounded">491</span>
            </a>
        </li>
    </ul>
</div>
<!-- Navigation Tabs -->

<!-- Tabs content -->
<div class="tab-content mx-5" id="ex1-content">
    <div class="tab-pane fade show active" id="ex1-tabs-1" role="tabpanel" aria-labelledby="ex1-tab-1">
        <div class="card">
            <div class="row m-3">
                @*First Column*@
                <div class="col-lg-4 col-md-12 col-sm-12">
                    <div class="row mb-2 ">
                        <div class="col">
                            <label><strong>Plant</strong></label>
                        </div>
                        <div class="col">
                            <div class="">
                                <select class="form-control" style="width: 100%;">
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
                            <label><strong>Material Type</strong></label>
                        </div>
                        <div class="col">
                            <div class="">
                                <select class="form-control" style="width: 100%;">
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
                </div>
                @*End First Column*@

                @*Second Column*@
                <div class="col-lg-5 col-md-12 col-sm-12">
                    <div class="row">
                        <div class="col">
                            <label><strong>Warehouse</strong></label>
                        </div>
                        <div class="col">
                            <div class="form-group">
                                <select class="form-control" style="width: 100%;">
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
                            <label><strong>Search Item</strong></label>
                        </div>
                        <div class="row mb-2">
                            <form class="form-inline">
                                <input class="form-control rounded-pill" type="search" placeholder="Search by item name or item code" aria-label="Search" style="width:400px;">
                            </form>
                        </div>
                    </div>
                </div>
                @*End of Second Section*@

                @*Third Column*@
                <div class="col-lg-3 col-md-12 col-sm-12">
                    <div class="row mb-2">
                        <div class="col">
                            <label><strong>Date:</strong></label>
                        </div>
                        <div class="col">
                            <input id="" name="" type="date" class="form-control" aria-label="Select Date">
                        </div>
                    </div>
                </div>
                @*End of Third Column*@
            </div>

            <hr />

            @*Start of Table Section*@
            <div class="row m-3">
                <div class="col">
                    <table class="col-6 table table-bordered">
                        <thead>
                            <tr>
                                <th scope="col"></th>
                                <th scope="col">From</th>
                                <th scope="col">To</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <th scope="row">Floor</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>

                            </tr>
                            <tr>
                                <th scope="row">Area</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>

                            </tr>
                            <tr>
                                <th scope="row">Section</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                            </tr>
                            <tr>
                                <th scope="row">Tank</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                            </tr>
                            <tr>
                                <th scope="row">Bay</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                            </tr>
                            <tr>
                                <th scope="row">Rack</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                            </tr>
                            <tr>
                                <th scope="row">Level</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                            </tr>
                            <tr>
                                <th scope="row">Deep</th>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                                <td><input type="text" class="form-control" id="" placeholder=""></td>
                            </tr>
                            <tr>
                                <th scope="row"></th>
                                <td colspan="2">
                                    <div class="text-right">
                                        <button class="btn btn-primary" data-toggle="modal" data-target="#generateModal" style="width:7rem;"><i class="fa fa-download"></i> Generate</button>
                                        <div class="modal fade" id="generateModal" tabindex="-1" role="dialog" aria-labelledby="generateModalLabel" aria-hidden="true">
                                            <div class="modal-dialog modal-lg" role="document">
                                                <div class="modal-content">
                                                    <div class="modal-header">
                                                        <h5 class="modal-title" id="generateModalLabel">Confirmation</h5>
                                                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                                                            <span aria-hidden="true">&times;</span>
                                                        </button>
                                                    </div>
                                                    <div class="modal-body text-left">
                                                        <p>Please review all data before proceeding.</p>
                                                        <div class="row">
                                                            <div class="col">
                                                                <div class="row mb-2">
                                                                    <div class="col">
                                                                        <label><strong>Plant:</strong></label>
                                                                    </div>
                                                                    <div class="col">
                                                                        <p>Canlubang</p>
                                                                    </div>
                                                                </div>

                                                                <div class="row mb-2">
                                                                    <div class="col">
                                                                        <label><strong>Material Type:</strong></label>
                                                                    </div>
                                                                    <div class="col">
                                                                        <p>All Material Type</p>
                                                                    </div>
                                                                </div>
                                                            </div>

                                                            <div class="col">
                                                                <div class="row mb-2">
                                                                    <div class="col">
                                                                        <label><strong>Warehouse:</strong></label>
                                                                    </div>
                                                                    <div class="col">
                                                                        <p>Building 2</p>
                                                                    </div>
                                                                </div>

                                                                <div class="row mb-2">
                                                                    <div class="col">
                                                                        <label><strong>Items:</strong></label>
                                                                    </div>
                                                                    <div class="col">
                                                                        <p>All Items</p>
                                                                    </div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                        <table class="table table-striped">
                                                            <thead class="bold">
                                                                <tr>
                                                                    <th scope="col"></th>
                                                                    <th scope="col">From</th>
                                                                    <th scope="col">To</th>
                                                                </tr>
                                                            </thead>
                                                            <tbody>
                                                                <tr>
                                                                    <td>Floor</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Area</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Section</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Tank</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Bay</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Rack</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Level</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                                <tr>
                                                                    <td>Deep</td>
                                                                    <td></td>
                                                                    <td></td>
                                                                </tr>
                                                            </tbody>
                                                        </table>
                                                    </div>

                                                    <div class="modal-footer">
                                                        <button type="button" class="btn btn-success" data-dismiss="modal"><i class="fa fa-check"></i> Yes</button>
                                                        <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times"></i> No</button>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
            @*End of Table Section*@
        </div>
    </div>

    <div class="tab-pane fade" id="ex1-tabs-2" role="tabpanel" aria-labelledby="ex1-tab-2">
        <div class="col-lg-6 col-md-12 col-sm-12">
            <div class="row mb-2 ">
                <div class="col">
                    <label><strong>Filter by Warehouse</strong></label>
                </div>
                <div class="col">
                    <div class="form-group">
                        <select class="form-control" style="width: 100%;">
                            <option selected>All Plants</option>
                            <option value="1">Canlubang</option>
                            <option value="2">Valenzuela</option>
                            <option value="3">Laguna</option>
                            <option value="3">IPIC</option>
                        </select>
                    </div>
                </div>

            </div>
        </div>

        @*Start of Search Bar*@
        <div class="ml-auto mb-2">
            <form class="form-inline d-flex justify-content-end">
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
                            <th>Ref Id</th>
                            <th>Plant</th>
                            <th>Warehouse</th>
                            <th>Prepared By</th>
                            <th>Encoded Date</th>
                            <th>Action</th>
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

    <div class="tab-pane fade" id="ex1-tabs-3" role="tabpanel" aria-labelledby="ex1-tab-3">
        <div class="col-lg-6 col-md-12 col-sm-12">
            <div class="row mb-2 ">
                <div class="col">
                    <label><strong>Filter by Warehouse</strong></label>
                </div>
                <div class="col">
                    <div class="form-group">
                        <select class="form-control" style="width: 100%;">
                            <option selected>All Plants</option>
                            <option value="1">Canlubang</option>
                            <option value="2">Valenzuela</option>
                            <option value="3">Laguna</option>
                            <option value="3">IPIC</option>
                        </select>
                    </div>
                </div>
            </div>
        </div>

        @*Start of Search Bar*@
        <div class="ml-auto mb-2">
            <form class="form-inline d-flex justify-content-end">
                <input class="form-control" type="search" placeholder="Search" aria-label="Search" style="width:400px;">
            </form>
        </div>
        @*End of Search Bar*@

        @*Table section*@
        <div class="row">
            <div class="col-12 table-responsive">
                <table id="Table2" class="table table-striped table-bordered">
                    <thead>
                        <tr>
                            <th>Ref Id</th>
                            <th>Plant</th>
                            <th>Warehouse</th>
                            <th>Prepared By</th>
                            <th>Encoded Date</th>
                            <th>Action</th>
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

    <div class="tab-pane fade" id="ex1-tabs-4" role="tabpanel" aria-labelledby="ex1-tab-4">
        <div class="col-lg-6 col-md-12 col-sm-12">
            <div class="row mb-2 ">
                <div class="col">
                    <label><strong>Filter by Warehouse</strong></label>
                </div>
                <div class="col">
                    <div class="form-group">
                        <select class="form-control" style="width: 100%;">
                            <option selected>All Plants</option>
                            <option value="1">Canlubang</option>
                            <option value="2">Valenzuela</option>
                            <option value="3">Laguna</option>
                            <option value="3">IPIC</option>
                        </select>
                    </div>
                </div>
            </div>
        </div>

        @*Start of Search Bar*@
        <div class="ml-auto mb-2">
            <form class="form-inline d-flex justify-content-end">
                <input class="form-control" type="search" placeholder="Search" aria-label="Search" style="width:400px;">
            </form>
        </div>
        @*End of Search Bar*@

        @*Table section*@
        <div class="row">
            <div class="col-12 table-responsive">
                <table id="Table3" class="table table-striped table-bordered table-hover">
                    <thead>
                        <tr>
                            <th>Ref Id</th>
                            <th>Plant</th>
                            <th>Warehouse</th>
                            <th>Prepared By</th>
                            <th>Encoded Date</th>
                            <th>Action</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>PC-0000000582</td>
                            <td>Canlubang</td>
                            <td>Building 2</td>
                            <td>SYSTEM ADMIN</td>
                            <td>3/17/2023</td>
                            <td class="text-center">
                                <button type="button" class="btn btn-primary">View</button>
                                <button type="button" class="btn btn-info">Download</button>
                                <button type="button" class="btn btn-warning"  data-toggle="modal" data-target="#printModal">Print</button>
                                <div class="modal fade" id="printModal" tabindex="-1" role="dialog" aria-labelledby="printModalLabel" aria-hidden="true">
                                    <div class="modal-dialog modal-lg" >
                                        <div class="modal-content">
                                            <div class="modal-header">  
                                                <h3>Physical Count</h3>
                                            </div>
                                            <div class="modal-body text-center">
                                            </div>
                                            <div class="modal-footer">
                                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times"></i> Close</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>PC-0000000582</td>
                            <td>Canlubang</td>
                            <td>Building 2</td>
                            <td>SYSTEM ADMIN</td>
                            <td>3/17/2023</td>
                            <td class="text-center">
                                <button type="button" class="btn btn-primary">View</button>
                                <button type="button" class="btn btn-info">Download</button>
                                <button type="button" class="btn btn-warning" data-toggle="modal" data-target="#printModal">Print</button>
                                <div class="modal fade" id="printModal" tabindex="-1" role="dialog" aria-labelledby="printModalLabel" aria-hidden="true">
                                    <div class="modal-dialog modal-lg">
                                        <div class="modal-content">
                                            <div class="modal-header">
                                                <h3>Physical Count</h3>
                                            </div>
                                            <div class="modal-body text-center">
                                            </div>
                                            <div class="modal-footer">
                                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times"></i> Close</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>PC-0000000582</td>
                            <td>Canlubang</td>
                            <td>Building 2</td>
                            <td>SYSTEM ADMIN</td>
                            <td>3/17/2023</td>
                            <td class="text-center">
                                <button type="button" class="btn btn-primary">View</button>
                                <button type="button" class="btn btn-info">Download</button>
                                <button type="button" class="btn btn-warning" data-toggle="modal" data-target="#printModal">Print</button>
                                <div class="modal fade" id="printModal" tabindex="-1" role="dialog" aria-labelledby="printModalLabel" aria-hidden="true">
                                    <div class="modal-dialog modal-lg">
                                        <div class="modal-content">
                                            <div class="modal-header">
                                                <h3>Physical Count</h3>
                                            </div>
                                            <div class="modal-body text-center">
                                            </div>
                                            <div class="modal-footer">
                                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times"></i> Close</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>PC-0000000582</td>
                            <td>Canlubang</td>
                            <td>Building 2</td>
                            <td>SYSTEM ADMIN</td>
                            <td>3/17/2023</td>
                            <td class="text-center">
                                <button type="button" class="btn btn-primary">View</button>
                                <button type="button" class="btn btn-info">Download</button>
                                <button type="button" class="btn btn-warning" data-toggle="modal" data-target="#printModal">Print</button>
                                <div class="modal fade" id="printModal" tabindex="-1" role="dialog" aria-labelledby="printModalLabel" aria-hidden="true">
                                    <div class="modal-dialog modal-lg">
                                        <div class="modal-content">
                                            <div class="modal-header">
                                                <h3>Physical Count</h3>
                                            </div>
                                            <div class="modal-body text-center">
                                            </div>
                                            <div class="modal-footer">
                                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times"></i> Close</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>PC-0000000582</td>
                            <td>Canlubang</td>
                            <td>Building 2</td>
                            <td>SYSTEM ADMIN</td>
                            <td>3/17/2023</td>
                            <td class="text-center">
                                <button type="button" class="btn btn-primary">View</button>
                                <button type="button" class="btn btn-info">Download</button>
                                <button type="button" class="btn btn-warning" data-toggle="modal" data-target="#printModal">Print</button>
                                <div class="modal fade" id="printModal" tabindex="-1" role="dialog" aria-labelledby="printModalLabel" aria-hidden="true">
                                    <div class="modal-dialog modal-lg">
                                        <div class="modal-content">
                                            <div class="modal-header">
                                                <h3>Physical Count</h3>
                                            </div>
                                            <div class="modal-body text-center">
                                            </div>
                                            <div class="modal-footer">
                                                <button type="button" class="btn btn-danger" data-dismiss="modal"><i class="fa fa-times"></i> Close</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
        @*End of Table section*@

        @*Dropdown Number/Pagination section*@
        <div class="row">
            <div class="col">
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
            </div>

            <div class="col d-flex justify-content-end mt-3">
                <nav aria-label="Page navigation example">
                    <ul class="pagination">
                        <li class="page-item">
                            <a class="page-link" href="#" aria-label="Previous">
                                <span aria-hidden="true">&laquo;</span>
                            </a>
                        </li>
                        <li class="page-item"><a class="page-link" href="#">1</a></li>
                        <li class="page-item"><a class="page-link" href="#">2</a></li>
                        <li class="page-item"><a class="page-link" href="#">3</a></li>
                        <li class="page-item">
                            <a class="page-link" href="#" aria-label="Next">
                                <span aria-hidden="true">&raquo;</span>
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        @*End Dropdown Number/Pagination section*@
    </div>
</div>

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

        $('#Table2').DataTable({
            dom: "",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
        });

        $('#Table3').DataTable({
            dom: "",
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
        });
    });
</script>

<style>
    .card .nav .nav-link {
        border-right: 1px solid #B8B8B8;
        border-radius: 0;
    }
    .card .nav .nav-link{
        color: black !important;
        font-size: 1rem;
        padding: 0.8rem;
    }

    .card .nav .active{
        color: whitesmoke !important;
    }
</style>
```

**Controllers**
```md title="File Location: Controllers/Inventory/PhysicalCount/PhysicalCountController.cs"
public IActionResult PhysicalCountV2()
        {
            return View("~/Views/Inventory/PhysicalCount/PhysicalCountV2.cshtml");
        }
```
