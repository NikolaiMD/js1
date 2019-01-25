<script type="text/javascript">
  const PRICE_SUSHI = 300;
  const PRICE_BORSCH = 30;
  const PRICE_PIZZA = 60;
  const PRICE_WINE = 100;
  const PRICE_COLA = 10;
  const PRICE_COFFEE = 200;
  const MENU =`##########
  ----FOOD----
  1.Sushi----${PRICE_SUSHI}MDL
  2.Borsch----${PRICE_BORSCH}MDL
  3.Pizza----${PRICE_PIZZA}MDL
  ----DRINKS----
  4.Wine----${PRICE_WINE}MDL
  5.Cola----${PRICE_COLA}MDL
  6.Coffee----${PRICE_COFFEE}MDL

  0.Complete order/Exit
  ##########`;
  var total_cost=0;
  while(true){
  var option=prompt(MENU);
    if(option==0){
      alert(`Your order total is ${total_cost}Thank you!`);
      break;
    }
  if(option<1||option>6){
    alert("WRONG OPTION!")
  }else{
    var quantity=prompt("HOW MANY?");
    var price=0;
    if(option==1) price=PRICE_SUSHI;
    if(option==2) price=PRICE_BORSCH;
    if(option==3) price=PRICE_PIZZA;
    if(option==4) price=PRICE_WINE;
    if(option==5) price=PRICE_COLA;
    if(option==6) price=PRICE_COFFEE;

    var cost=quantity*price;
    var ok=confirm(`${quantity} portion(s) will cost you ${cost}MDL. Do you agree to continue?`);
    if(ok==true){
      total_cost += cost;
    }
    console.log(ok);
  }
}
// Discount/free delivery>=500mdl
</script>
