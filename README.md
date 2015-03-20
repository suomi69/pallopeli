/* 
 * peli.js
 */
(function() {
    var ladatutLkm;
	var ajastin;
    var tausta;
	var palloKuva;
    var pallo=new Pallo(50,400,3);
    var pallopiirto;
	var pylvaat=new Array();
	var pylvasKuvat=new Array();
    var pylvas={
                x: 0,
                y: 0
              };

    lataa();

    function lataa() {
        ladatutLkm=0;
        tausta=new Image();
        tausta.src='kuvat/tausta2.png';
        tausta.onload=olenValmis;
        
        palloKuva=new Image();
        palloKuva.src='kuvat/pallo.png';
        palloKuva.onload=olenValmis;
        
        var pylvas1=new Image;
        pylvas1.src='kuvat/pylvas1.png';
        pylvas1.onload=olenValmis;
		pylvasKuvat.push(pylvas1);
        
        var pylvas2=new Image;
        pylvas2.src='kuvat/pylvas1.png';
        pylvas2.onload=olenValmis;
		pylvasKuvat.push(pylvas2);
        
        var pylvas3=new Image;
        pylvas3.src='kuvat/pylvas1.png';
        pylvas3.onload=olenValmis;
		pylvasKuvat.push(pylvas3);
        
        var pylvas4=new Image;
        pylvas4.src='kuvat/pylvas2.png';
        pylvas4.onload=olenValmis;
		pylvasKuvat.push(pylvas4);
                
        var pylvas5=new Image;
        pylvas5.src='kuvat/pylvas1.png';
        pylvas5.onload=olenValmis;
		pylvasKuvat.push(pylvas5);
          
        var pylvas6=new Image;
        pylvas6.src='kuvat/pylvas2.png';
        pylvas6.onload=olenValmis;
		pylvasKuvat.push(pylvas6);
        
        var pylvas7=new Image;
        pylvas7.src='kuvat/pylvas1.png';
        pylvas7.onload=olenValmis;
		pylvasKuvat.push(pylvas7);
        
        var pylvas8=new Image;
        pylvas8.src='kuvat/pylvas2.png';
        pylvas8.onload=olenValmis;
		pylvasKuvat.push(pylvas8);
		
		var pylvas9=new Image;
        pylvas9.src='kuvat/pylvas2.png';
        pylvas9.onload=olenValmis;
		pylvasKuvat.push(pylvas9);
		
		var pylvas10=new Image;
        pylvas10.src='kuvat/pylvas1.png';
        pylvas10.onload=olenValmis;
		pylvasKuvat.push(pylvas10);
		
		var pylvas11=new Image;
        pylvas11.src='kuvat/pylvas1.png';
        pylvas11.onload=olenValmis;
		pylvasKuvat.push(pylvas11);
		
		var pylvas12=new Image;
        pylvas12.src='kuvat/pylvas2.png';
        pylvas12.onload=olenValmis;
		pylvasKuvat.push(pylvas12);
		
		var pylvas13=new Image;
        pylvas13.src='kuvat/pylvas1.png';
        pylvas13.onload=olenValmis;
		pylvasKuvat.push(pylvas13);
		
		var pylvas14=new Image;
        pylvas14.src='kuvat/pylvas1.png';
        pylvas14.onload=olenValmis;
		pylvasKuvat.push(pylvas14);
		
		var pylvas15=new Image;
        pylvas15.src='kuvat/pylvas1.png';
        pylvas15.onload=olenValmis;
		pylvasKuvat.push(pylvas15);
		
		var pylvas16=new Image;
        pylvas16.src='kuvat/pylvas2.png';
        pylvas16.onload=olenValmis;
		pylvasKuvat.push(pylvas16);
		
		var pylvas17=new Image;
        pylvas17.src='kuvat/pylvas2.png';
        pylvas17.onload=olenValmis;
		pylvasKuvat.push(pylvas17);
		
		var pylvas18=new Image;
        pylvas18.src='kuvat/pylvas2.png';
        pylvas18.onload=olenValmis;
		pylvasKuvat.push(pylvas18);
		
		var pylvas19=new Image;
        pylvas19.src='kuvat/pylvas1.png';
        pylvas19.onload=olenValmis;
		pylvasKuvat.push(pylvas19);
		
		var pylvas20=new Image;
        pylvas20.src='kuvat/pylvas1.png';
        pylvas20.onload=olenValmis;
		pylvasKuvat.push(pylvas20);
    };
	
    function olenValmis() {
        if(++ladatutLkm===22) {
        piirraTausta();
		piirraPallo();
		luoPylvaat();
        piirraPylvaat();
        lisaaNappis();
		ajastin=setInterval(paivitaPeli,10); 
        }
    };
	
	function paivitaPeli() {
		pallo.paivitaPaikka();
		tarkastaTormays();
		//lisaaPylvaat();
		tarkastaRajat();
		piirraPylvaat();
		piirraPallo();
	};
	
	function tarkastaRajat(){
		pallo.tarkastaRaja();	
	}
	
	function piirraTausta() {
			var taustapiirto=document.getElementById('tausta');
			var konteksti=taustapiirto.getContext("2d");
			konteksti.drawImage(tausta, 0,0);
   	};
	
	function luoPylvaat(){
			pylvaat.push(new Pylvas(150,400));
			pylvaat.push(new Pylvas(300,400));
			pylvaat.push(new Pylvas(450,400));
			pylvaat.push(new Pylvas(600,500));
			pylvaat.push(new Pylvas(750,400));
            pylvaat.push(new Pylvas(900,500));
            pylvaat.push(new Pylvas(1050,400));
            pylvaat.push(new Pylvas(1200,500));
			pylvaat.push(new Pylvas(1350,500));
			pylvaat.push(new Pylvas(1500,400));
			pylvaat.push(new Pylvas(1650,400));
			pylvaat.push(new Pylvas(1800,500));
			pylvaat.push(new Pylvas(1950,400));
			pylvaat.push(new Pylvas(2100,400));
			pylvaat.push(new Pylvas(2250,400));
			pylvaat.push(new Pylvas(2400,500));
			pylvaat.push(new Pylvas(2550,500));
			pylvaat.push(new Pylvas(2700,500));
			pylvaat.push(new Pylvas(2850,400));
			pylvaat.push(new Pylvas(3000,400));
	};
		
	function paivitaPylvaidenPaikat(){
		//var vika=pylvaat[pylvaat.length-1].getSarake();
			for(var i=0; i<pylvaat.length;i++) {
					pylvaat[i].paivitaPaikka();
					//if(pylvaat[i].getSarake()<0){
						//pylvaat[i].setSarake(vika);	
						//vika+=150;
					//}
			}
	};
	
	function piirraPylvaat(){
			var pylvaspiirto=document.getElementById('pylvaat');
			var konteksti=pylvaspiirto.getContext("2d");
			konteksti.clearRect(0,0,pylvaspiirto.width,pylvaspiirto.height);
			for(var i=0; i<pylvaat.length;i++) {
				var pylvas=pylvaat[i];
				konteksti.drawImage(pylvasKuvat[i], pylvas.getSarake(), pylvas.getRivi());
			}
	};
	
    function piirraPallo() {
			pallopiirto=document.getElementById('pallo');
			var konteksti=pallopiirto.getContext("2d");
			konteksti.clearRect(0,0,pallopiirto.width,pallopiirto.height);
			konteksti.drawImage(palloKuva, pallo.getSarake(),pallo.getRivi());
   	};	
        
	function tarkastaTormays() {
            for(var i=0; i<pylvaat.length;i++) {
				if (pylvaat[i].getYmparoivaNelio().vertaa(pallo.getYmparoivaNelio())){
				pallo.osui();
				}
            }
    };
	
 	function suoritaToiminto(toiminto){
        	paivitaPylvaidenPaikat();		

    };

    function lisaaNappis() {
        	console.log("lisää");
			var nappaimisto=new Nappainkonfiguraatio();
			nappaimisto.lisaaNappain(NAPPAIN.NUOLI_VASEN,TOIMINTO.VASEN);
        	window.addEventListener('keydown', function(e){
           		suoritaToiminto(nappaimisto.getToiminto(e.keyCode)); 
        	});
    };
	
})();
