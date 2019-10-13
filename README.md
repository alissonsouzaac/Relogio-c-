# Relogio-c-
#include "Relogio.h"
#include <string>
#include <iostream>
using namespace std;
Relogio::Relogio() {
    hora=0;
    minuto=0;
    segundo=0;
}
Relogio::Relogio(int h, int m, int s){

    if(s >= 1 && s <= 60){

        segundo = s;

    }else{

        std::cout << "Nao existe esse horario" << std::endl;
    }

    if(m >= 1 && m <= 60){

        minuto = m;

    }else{

        std::cout << "nao existe esse horario" << std::endl;
    }
    if(h >= 1 && h <= 24){

        hora = h;

    }else{

        std::cout << "nao existe esse horario" << std::endl;
    }


}

int Relogio::avancarHorario(){

        if(segundo<60){
        segundo++;
        }
        if(segundo==60){
            segundo = 0;
            minuto++;
        }

        if(minuto==60){
            minuto=0;
            hora++;
        }

        if(hora==24){
            hora=0;
        }


}
