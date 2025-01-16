# ASP.NET-Core-Web-App-Model-View-Controller

### 2025-1-16
- အတိုကောက်ကတော့ MVC
- Model
- View
- Controller
- ဒီလိုပြောလို့ Model က အရင်လာတာ မဟုတ်ဘူး Controller က အရင်လာတာပါ။
  

- Controller => Logic => Processing => Data => Model => View (UI).

- View (Submit) => Controller with (Model) => Processing => Data => View (UI).

- ဒီမှာ Client နဲ့ Server ဆိုပြီးရှိပါတယ်။

- Client ဆိုတာ View ပါ။
- Server ဆိုတာ Controller ပါ။

- MVC ရဲ့ program.cs မှာ ဆိုရင်
- app.UseRouting();
- app.UseAuthorization();
- app.MapControllerRout();
တို့ကို တွေ့ရမှာ ဖြစ်ပါတယ်။

ဒီထဲမှာမှ app.MapControllerRout();မှာ သတိထားရမှာလေးတွေရှိပါတယ်။ 

pattern: "{controller=Home}/{action=Index}/{id?}"

id မှာ ? က id ပါလည်းရတယ်၊ မပါလည်းရတယ်ဆိုတဲ့ သဘောပါ။ 

url က
https://localhost:localhost3000/Home/Index/1 ဆိုပါစို့။ 

Controller က နေ ယူမယ်ဆိုရင် method(int id) or method(string id)
ဆိုပြီး ဖြစ်တယ်။ 

အကယ်၍ method ကသာ method(string blogId) and  method(int userId) ဆိုရင်

url က 
https://localhost:localhost3000/Home/Index?blogId=1 and https://localhost:localhost3000/Home/Index?userId=1  ဖြစ်သွားမှာပါ။ 






