<?php
  
class nodo{
  
   public $dato;
   public $siguiente;
   public function __construct($dato)
   {
     $this-> dato = $dato;
     $this-> siguiente = null;
   }
}

class listaenlazada {
  
  public $cabeza;

  public function __construct(){
  $this->cabeza=null;  
  }

  public function insertar($dato)
  {
$nuevonodo=new nodo($dato);
$nuevonodo->siguiente=$this->cabeza;
$this->cabeza=$nuevonodo; 
  }

  public function imprimirHTML()
  {
$actual=$this->cabeza;
echo"<ul>";

while($actual!=null){
  echo "<li>".$actual->dato."</li>";
  $actual=$actual->siguiente;
}

echo"</ul>";

  }
}

$lista=new listaenlazada();

$lista->insertar("elemento1");
$lista->insertar("elemento2");
$lista->insertar("elemento3");
$lista->imprimirHTML();

?>
