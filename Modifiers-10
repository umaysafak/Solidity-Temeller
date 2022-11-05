// SPDX-License-Identifier: MIT

pragma solidity ^0.8.15;

contract modifiers {

    uint sayi;
    address kullanici;
    //uint tipinde sayi ve address tipinde kullanici oluşturuldu

    constructor() {
        kullanici = msg.sender;
    }
    //constructor ile kullanici msg.sender'a eşitlendi(kontrat deploy edilirken bulunduğu addres)

    modifier isKullanici()  {
        require (msg.sender == kullanici, "you are not owner.");
        _;
    }
    //modifiere tipinde isKullanici oluşturularak eğer belirleyeceğimiz sayı deploy edilirken kullanılan address'ten başka
    //bir adres tarafından işlem yapılırsa "you are not owner" hatası vericeği belirlendi.
    
    function setSayi (uint _sayi) public isKullanici {
        sayi = _sayi;
    }
    //isKullanici modifier'ı setSayi fonksiyonuna eklenerek setSayi fonksiyonunun içine eklenen _sayi, sayi değerine eşitlendi

    function getSayi () public view isKullanici returns (uint) {
        return sayi;
    }
    //isKullanici modifier'ı getSayi fonksiyonuna eklenerek sayi değeri döndürüldü.

}
