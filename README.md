# Realidade Aumentada Unity

Aplicação Simples de Realidade Aumentada Unity + Vuforia

A combinação entre Unity e Vuforia oferece uma solução altamente eficaz para o desenvolvimento de aplicativos de realidade aumentada, possibilitando que os desenvolvedores criem experiências incríveis em AR para uma ampla variedade de aplicações

<img width="450" src="https://i.ibb.co/zPXGT5j/vuforia-unity-logo.png" alt="vuforia-unity-logo" border="0" />

(Colocar GIF)

Para desenvolver um aplicativo semelhante ao mencionado acima, é necessário fazer o download do Vuforia Engine.

| É possível importar o Vulforia para o Unity.

https://developer.vuforia.com/user/login?url=/downloads/sdk%3F_%3D1678117884 (arrumar)

| Para registrar o seu alvo (target) e seus recursos (features), é preciso criar uma conta e obter uma licença. Depois disso, faça o download do banco de dados que        | contém o seu alvo e seus recursos.

<img src="https://i.ibb.co/T00xSB4/Target.png" alt="Target" border="0">

<img src="https://i.ibb.co/9VxfJ6T/target-mapeada.png" alt="target-mapeada" border="0">

| A Figura acima mostra o mapeamento para realidade aumentada.

**Monte sua cena:**

| Incluindo o Imagem Target e a Câmera AR

<img src="https://i.ibb.co/X8rGZ9n/img-unity.png" alt="img-unity" border="0">

'''javascript'''

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class rotate : MonoBehaviour
{
    public Vector3 rotateAmount;
    void Start()
    {
        
    }

    void Update()
    {
        transform.Rotate(rotateAmount * Time.deltaTime);
    }
}

'''javascript'''
