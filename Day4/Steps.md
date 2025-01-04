

Step1: create a new app called "app2"
Step2:![image](https://github.com/user-attachments/assets/1c62888a-caf7-41d2-aff2-f8494e14f9e2)

Step3:
![image](https://github.com/user-attachments/assets/b7928f3e-a02f-41bf-a125-0e498f584f14)
![image](https://github.com/user-attachments/assets/c69a7357-04e1-4868-98b9-059a98b3eb4f)


Step4:
from django.shortcuts import render
from django.http import HttpResponse, JsonResponse
from app2.models import Product

# Create your views here.
def pro_records(request):
    """
    with this model we try to return all product model record as API
    """
    pro_data = Product.objects.all()
    response = []
    for rec in pro_data:
        response.append({
            "Name_of_Product": rec.pro_name,
            "Price": rec.pro_price,
            "Description": rec.pro_desc,
            "Ratings":rec.rating,
        })
    return JsonResponse(response, safe=False)
![image](https://github.com/user-attachments/assets/995eb93e-427b-48a6-b145-79df82ff91b5)
![image](https://github.com/user-attachments/assets/921e171c-3f55-4fb6-afc6-13fea9aa5086)


Step5:
![image](https://github.com/user-attachments/assets/03d3a83f-c6cd-4876-8cb2-1df4509669d1)
![image](https://github.com/user-attachments/assets/5ee9b4ef-b279-46a6-9194-09bdd10512a7)


Step6:
![image](https://github.com/user-attachments/assets/8860a9d3-70fa-40dc-99cb-ea57da59114d)
![image](https://github.com/user-attachments/assets/9b9610be-f43b-43d5-a903-b793e106b487)



Step7:
![image](https://github.com/user-attachments/assets/386e27e1-4364-404d-80e4-990aa068b733)

Postman
![image](https://github.com/user-attachments/assets/ee888d90-dcb5-4e74-b9ad-3cd66abedb90)
![image](https://github.com/user-attachments/assets/17765c38-f6ce-4cac-afd7-347c189ade53)


Step8:
Step9:
Step10:


