### StockCardV2
**Views**
```md title="File Location: Views/Inventory/StockCard/StockCardV2.cshtml"

@{
    ViewData["Title"] = "StockCardV2";
    Layout = "~/Views/Shared/_Layout.cshtml";
}
<link href="~/css/stock-card.css" rel="stylesheet"/>

<div class="stockCardTitle">
    <h4>Stock Card V2</h4>
</div>

<div class="stockCardContainer">
    <div class="searchTab">
        <label class="font-weight-bold">Search Item</label>
        <div class="ui fluid icon input">
            <input placeholder="Search by item name or item code" type="text" tabindex="0" class="prompt" autocomplete="off" value="">
            <i aria-hidden="true" class="search icon"></i>
        </div>
    </div>

    <div class="stockCardContainerTwo">
        <div class="infoGrid">
            <div class="leftGrid">
                <div class="labelInfo">
                    <label class="font-weight-bold">Item Code</label>
                    <label></label>
                </div>

                <div class="labelInfo">
                    <label class="font-weight-bold">Base Unit</label>
                    <label></label>
                </div>

                <div class="labelInfo">
                    <label class="font-weight-bold">Description</label>
                    <label></label>
                </div>

                <div class="labelInfo">
                    <label class="font-weight-bold">Status</label>
                    <label></label>
                </div>
            </div>

            <div class="rightGrid">
                <div class="labelInfo">
                    <label class="font-weight-bold">Minimum Stock Level</label>
                    <label>0</label>
                </div>

                <div class="labelInfo">
                    <label class="font-weight-bold">Total On Hand</label>
                    <label>0</label>
                </div>

                <div class="labelInfo">
                    <label class="font-weight-bold">Total Reserved</label>
                    <label>0</label>
                </div>

                <div class="labelInfo">
                    <label class="font-weight-bold">Total Balance</label>
                    <label>0</label>
                </div>
            </div>
        </div>

        <div class="ui divider">

        </div>

        <div>
            <!-- Tabs navs -->
            <ul class="nav nav-pills" id="ex1" role="tablist">
                <li class="nav-item tabName" role="presentation">
                    <a class="nav-link active"
                       id="ex1-tab-1"
                       data-toggle="tab"
                       href="#ex1-tabs-1"
                       role="tab"
                       aria-controls="ex1-tabs-1"
                       aria-selected="true">Total Summary</a>
                </li>
                <li class="nav-item tabName" role="presentation">
                    <a class="nav-link"
                       id="ex1-tab-2"
                       data-toggle="tab"
                       href="#ex1-tabs-2"
                       role="tab"
                       aria-controls="ex1-tabs-2"
                       aria-selected="false">Stock On Hand</a>
                </li>
                <li class="nav-item tabName" role="presentation">
                    <a class="nav-link"
                       id="ex1-tab-3"
                       data-toggle="tab"
                       href="#ex1-tabs-3"
                       role="tab"
                       aria-controls="ex1-tabs-3"
                       aria-selected="false">Stock Ledger</a>
                </li>
                <li class="nav-item tabName" role="presentation">
                    <a class="nav-link"
                       id="ex1-tab-4"
                       data-toggle="tab"
                       href="#ex1-tabs-4"
                       role="tab"
                       aria-controls="ex1-tabs-4"
                       aria-selected="false">Item Serials</a>
                </li>
            </ul>
            <!-- Tabs navs -->
            <!-- Tabs content -->
            <div class="tab-content" id="ex1-content">
                <div class="tab-pane fade show active" id="ex1-tabs-1" role="tabpanel" aria-labelledby="ex1-tab-1">
                    <div class="summaryGrid">
                        <div class="tabInfo">
                            <label class="font-weight-bold">Total Purchase Request Quantity</label>
                            <label>0</label>
                        </div>
                        <div class="tabInfo">
                            <label class="font-weight-bold">Total Ordered Purchase Request Quantity</label>
                            <label>0</label>
                        </div>
                        <div class="tabInfo">
                            <label class="font-weight-bold">Total Incoming In-Transit Quantity</label>
                            <label>0</label>
                        </div>
                    </div>
                </div>
                <div class="tab-pane fade" id="ex1-tabs-2" role="tabpanel" aria-labelledby="ex1-tab-2">
                    <div class="stockOnHoldContainer">
                        <div class="stockOnHoldGrid">
                            <div class="leftGrid">
                                <div class="tabInfo">
                                    <label>Display UOM</label>
                                    <div id="itemUnitId2" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Search item unit</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>
                            </div>

                            <div class="rightGrid">
                                <div class="tabInfo">
                                    <label>Filter by Plant</label>
                                    <div id="shPlant" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Filter by Plant</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Filter by Warehouse</label>
                                    <div id="shWarehouse" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Filter by Plant</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Filter by Location</label>
                                    <div id="shLocation" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        @*<div class="text" role="alert" aria-live="polite" aria-atomic="true">Filter by Plant</div>*@
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="stockButtons">
                                    <button title="" class="ui green mini icon disabled left labeled button font-mini" disabled="" tabindex="-1">
                                        <i aria-hidden="true" class="filter icon"></i>
                                        Filter
                                    </button>
                                    <button title="" class="ui red mini icon disabled left labeled button font-mini" disabled="" tabindex="-1">
                                        <i aria-hidden="true" class="filter icon"></i>
                                        Clear Filter
                                    </button>
                                </div>
                            </div>
                        </div>

                        <div class="table-responsive">
                            <table class="table table-striped table-bordered" id="stockOnHandTable" cellspacing="0" width="100%">
                                <thead>
                                    <tr>
                                        <th>Warehouse</th>
                                        <th>Location</th>
                                        <th>On Hand</th>
                                        <th>Reserved</th>
                                        <th>Available Qty</th>
                                    </tr>
                                </thead>

                                <tbody>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>

                <div class="tab-pane fade" id="ex1-tabs-3" role="tabpanel" aria-labelledby="ex1-tab-3">
                    <div class="stockledgerContainer">
                        <div class="stockLedgerGrid">
                            <div class="leftGrid">
                                <div class="tabInfo">
                                    <label>Display UOM</label>
                                    <div id="itemUnitId" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Search item unit</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Filter by Plant</label>
                                    <div id="slPlant" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Filter by Plant</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Filter by Warehouse</label>
                                    <div id="slWarehouse" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Filter by Plant</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Filter by Location</label>
                                    <div id="slLocation" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        @*<div class="text" role="alert" aria-live="polite" aria-atomic="true">Filter by Plant</div>*@
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>
                            </div>

                            <div class="rightGrid">
                                <div class="tabInfo">
                                    <label>Movement Type</label>
                                    <div role="combobox" class="ui disabled search selection dropdown form-control">
                                        <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                                        <div class="text" role="alert" aria-live="polite" aria-atomic="true">Select Movement Type</div>
                                        <i aria-hidden="true" class="dropdown icon"></i>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Date From</label>
                                    <div class="react-bootstrap-daterangepicker-container" style="display: inline-block;">
                                        <button class="selected-date-range-btn form-control h-auto">
                                            <div class="pull-left">
                                                <i class="fa fa-calendar"></i>
                                            </div>
                                            
                                            <span class="text-center p-1">April 03, 2023</span>
                                            <div class="pull-right">
                                                <span><i class="fa fa-caret-down"></i></span>
                                            </div>
                                        </button>
                                    </div>
                                </div>

                                <div class="tabInfo">
                                    <label>Date To</label>
                                    <div class="react-bootstrap-daterangepicker-container" style="display: inline-block;">
                                        <button class="selected-date-range-btn form-control h-auto">
                                            <div class="pull-left">
                                                <i class="fa fa-calendar"></i>
                                            </div>

                                            <span class="text-center p-1">April 30, 2023</span>
                                            <div class="pull-right">
                                                <span><i class="fa fa-caret-down"></i></span>
                                            </div>
                                        </button>
                                    </div>
                                </div>

                                <div class="stockButtons">
                                    <button title="" class="ui green mini icon disabled left labeled button font-mini" disabled="" tabindex="-1">
                                        <i aria-hidden="true" class="filter icon"></i>
                                        Filter
                                    </button>
                                    <button title="" class="ui red mini icon disabled left labeled button font-mini" disabled="" tabindex="-1">
                                        <i aria-hidden="true" class="filter icon"></i>
                                        Clear Filter
                                    </button>
                                </div>
                            </div>
                        </div>

                        <div class="actualButton">
                            <div class="ui checkbox">
                                <input readonly="" tabindex="0" type="checkbox" value="">
                                <label>Show actual</label>
                            </div>
                        </div>

                        <div class="table-responsive">
                            <table class="table table-striped table-bordered" id="stockLedgerTable" cellspacing="0" width="100%">
                                <thead>
                                    <tr>
                                        <th></th>
                                        <th colspan="2">Item</th>
                                        <th>Movement</th>
                                        <th colspan="5">Quantity</th>
                                        <th colspan="2">Warehouse</th>
                                        <th>Location</th>
                                        <th colspan="2">Plant</th>
                                    </tr>

                                    <tr>
                                        <th>Date</th>
                                        <th>Code</th>
                                        <th>Unit</th>
                                        <th>Type</th>
                                        <th>Reference</th>
                                        <th>In</th>
                                        <th>Out</th>
                                        <th>Balance</th>
                                        <th>Reserved</th>
                                        <th>Available</th>
                                        <th>From</th>
                                        <th>To</th>
                                        <th>Code</th>
                                        <th>Name</th>
                                    </tr>
                                </thead>

                                <tbody>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>

                <div class="tab-pane fade" id="ex1-tabs-4" role="tabpanel" aria-labelledby="ex1-tab-4">
                    <div class="filterGrid">
                        <label>Filter by Warehouse</label>
                        <div id="serialWarehouse" class="ui disabled search selection dropdown form-control">
                            <input aria-autocomplete="list" autocomplete="off" class="search" tabindex="-1" type="text" value="">
                            <div class="text" role="alert" aria-live="polite" aria-atomic="true">All warehouse</div>
                            <i aria-hidden="true" class="dropdown icon"></i>
                        </div>
                    </div>

                    <div class="table-responsive">
                        <table class="table table-striped table-bordered" id="itemSerialsTable" cellspacing="0" width="100%">
                            <thead>
                                <tr>
                                    <th>Serial No.</th>
                                    <th>Warehouse</th>
                                    <th>Status</th>
                                </tr>
                            </thead>

                            <tbody>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
            <!-- Tabs content -->
        </div>
    </div>
</div>

<script>
    $(document).ready(function () {
        $('#stockOnHandTable').DataTable({
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
            dom: "<'mylength'l>tip",
        });

        $('#itemSerialsTable').DataTable({
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
            dom: "<'mylength'l>tip",
        });

        $('#stockLedgerTable').DataTable({
            ordering: true,
            select: {
                selector: 'td:not(:first-child)',
                style: 'os'
            },
            dom: "<'mylength'l>tip",
        });
    });
</script>
```

**Controllers**
```md title="File Location: Controllers/Inventory/StockCard/StockCardController.cs"
public IActionResult StockCardV2()
        {
            return View("~/Views/Inventory/StockCard/StockCardV2.cshtml");
        }
```
