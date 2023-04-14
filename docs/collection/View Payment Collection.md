### PaymentCollectionV2()
**Views**
```md title="File Location: Views/Collection/ViewPaymentCollection/ViewPaymentCollection.cshtml"
@model Base.Core.App.Models.Maintenance.FormDropdownData.FormDropdownData;
@using Microsoft.AspNetCore.Http
@{
    ViewData["Title"] = "ViewPaymentCollection";
}
<div class="card">
    <div class="row ml-2 mr-2">
        <div class="col-md-6 card-body">
            <h3 class="">
                View Collection
            </h3>
        </div>
        <div class="col-md-6 card-body text-right">
            <a class="" asp-controller="ViewPaymentCollection" asp-action="Index"><h3><i class="fa fa-times"></i><span class="cui-contrast"></span></h3></a>
        </div>
    </div>
</div>

<div id="view-payment-collection"></div>

<script>
     function urlParam(name) {
         var results = new RegExp('[\?&]' + name + '=([^&#]*)').exec(window.location.href);
            return results[1] || 0;
    }

    var collectionId = urlParam("collectionId");
    //console.log("collectionId", collectionId)


    function convert(model) {
        return JSON.stringify(model)
    };

    var data = {
        username: '@Context.Session.GetString("Fullname")',
        collectionId: collectionId,
        customers: convert(@Html.Raw(Json.Serialize(Model.customersSelectListItem)))
    }
</script>

<script src="~/dist/view_payment_collection.js"></script>
```

**Controllers**
```md title="File Location: Controllers/Collection/PaymentCollection/PaymendtCollectionController.cs"
public async Task<IActionResult> PaymentCollectionV2()
        {
            return View("~/Views/Collection/PaymentCollection/CollectPayments/PaymentCollectionV2.cshtml");
        }
```
