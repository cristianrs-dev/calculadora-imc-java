# calculadora-imc-java

https://eclipsecjp.github.io/calculadora-imc-java/



![CALC](https://github.com/eclipseCJP/calculadora-imc-java/assets/58758617/553cd104-aff6-4437-bd11-bbfe17d73f73)

 public void calcular(){
        float altura,peso,imc;
        String mensagem;
        altura = Float.parseFloat(h.getText());
        peso = Float.parseFloat(p.getText());
        
        imc = peso/(altura/100 * altura/100);
        
    // Gravando a Mensagem
    if(imc < 18.5){
        mensagem = name.getText()+ " Você está muito magro. Precisa de uma dieta para engordar";
    }else if(imc < 24.9){
        mensagem = name.getText()+ " Você está com peso ideal. Não precisa de dieta";
    }else if(imc < 29.9){
        mensagem = name.getText()+ " Você está com sobrepeso. Precisa de uma dieta para emagrecer";
    }else if(imc < 30){
        mensagem = name.getText()+ " Você está com obesidade. Precisa de uma dieta, exercícios e uma mudança de vida";
    }else {
        mensagem = name.getText()+ " Você está com obesidade grave. Precisa procurar um médico";
    }
        
        resposta.setText(mensagem);
    }
    
    public void limparCampo(){
        h.setText(null);
        p.setText(null);
        name.setText(null);
    }
}
