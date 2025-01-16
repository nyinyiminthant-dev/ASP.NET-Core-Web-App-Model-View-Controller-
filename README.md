# ASP.NET-Core-Web-App-Model-View-Controller

### 2025-1-16

### MVC Intro
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
  
### MVC Singnature

- MVC ရဲ့ program.cs မှာ ဆိုရင်
- app.UseRouting();
- app.UseAuthorization();
- app.MapControllerRout();
တို့ကို တွေ့ရမှာ ဖြစ်ပါတယ်။

### Notice

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

### project ကို စ run မယ်ဆိုရင်

pattern: "{controller=Home}/{action=Index}/{id?}"

pattern အရ home ထဲက index ကိုသွားမှာပါ။ အဲ့ဒီကို မသွားခင် _ViewStart.cshtml ကို စပြီး ရောက်မှာဖြစ်ပါတယ်။ 

_ViewStart.cshtml ထဲမှာ 
@{
 Layout = "_Layout";
}
အဲ့ဒီမှာ ""ထဲက _Layout ကို master page လို့ ခေါ်ပါတယ်။ 

### Master page

- master page ဆိုတာ page အတိုင်းအတွက် တူညီတဲ့ layout တွေကို ထပ်ခါထပ်ခါ ရေးစရာ မလိုအောင် layout ချထားတဲ့ page ဖြစ်ပါတယ်။ 

ဥပမာ header နဲ့ footer က page တိုင်းမှာ တူညီစွာ ရှိနေမယ်ဆိုရင် master page မှာ header နဲ့ footer ကို ရေးထားပြီး အခြား page တွေမှာ ရေးစရာမလိုပဲ body အပိုင်းကိုသာ ရေးရမှာဖြစ်ပါတယ်။ 


layout ချတဲ့နေရာမှာ mster page အတွက် _Layout.cshtml မှ မဟုတ်ပါဘူး ကိုယ်ကြိုက်တဲ့ နာမည်ကို ပေးနိုင်ပါတယ်။

ဥပမာ _AdimLayout.cshtml နဲ့ _ClientLayout.cshtml ရှိတယ်ဆိုပါစို့။ 

အဲ့ဒီလိုဆိုရင် Admin.cshtml မှာ 

@{
Layout = "_AdminLayout";
}

ဆိုပြီးခေါ်ပေးရမှာ ဖြစ်ပါတယ်။ Client.cshtml လည်း ထိုနည်းတူစွာ ဖြစ်ပါတယ်။ ကိုယ်သုံးချင်တဲ့ page မှာ ကိုယ်လိုချင်တဲ့ layout ကို ခေါ်သုံးနိုင်ပါတယ်။ 

အကယ်၍ Layout = "_Layout"; ဖြစ်မယ်ဆိုရင် ပြန်မခေါ်လည်း default အရ အလုပ်လုပ်နေမှာ ဖြစ်ပါတယ်။ 





