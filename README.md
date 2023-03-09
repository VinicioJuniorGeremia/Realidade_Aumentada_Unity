# Realidade Aumentada Unity

Aplicação Simples de Realidade Aumentada Unity + Vuforia

A combinação entre Unity e Vuforia oferece uma solução altamente eficaz para o desenvolvimento de aplicativos de realidade aumentada, possibilitando que os desenvolvedores criem experiências incríveis em AR para uma ampla variedade de aplicações

<img width="450" src="https://i.ibb.co/zPXGT5j/vuforia-unity-logo.png" alt="vuforia-unity-logo" border="0" />

<p>
  <img src="C:/Users/vinic/OneDrive/Documentos/Tecnologias Imersivas/gif do caramba.gif" width="598" height="336">
</p>>

Para desenvolver um aplicativo semelhante ao mencionado acima, é necessário fazer o download do Vuforia Engine.

| É possível importar o Vulforia para o Unity.

[Donwload Vulforia](https://developer.vuforia.com/user/login?url=/downloads/sdk%3F_%3D1678117884)

| Para registrar o seu alvo (target) e seus recursos (features), é preciso criar uma conta e obter uma licença. Depois disso, faça o download do banco de dados que      contém o seu alvo e seus recursos.

Após criar registrar uma licença no site da Vulforia e criar um banco de dados , faça o donwload do mesmo. Dentro do Unity, selecione a target e vincule o assinatura de licença e o banco de dados baixado.

<img src="https://i.ibb.co/T00xSB4/Target.png" alt="Target" border="0">

<img src="https://i.ibb.co/9VxfJ6T/target-mapeada.png" alt="target-mapeada" border="0">

| A Figura acima mostra o mapeamento para realidade aumentada.

**Monte sua cena:**

| Incluindo o Imagem Target e a Câmera AR

Para incluir, basta selecionar a imagem baixada e arrastar para dentro do Unity.

<img src="https://i.ibb.co/X8rGZ9n/img-unity.png" alt="img-unity" border="0">

Após criar a imagem target, adicione um cubo em cima dela, clicando com a parte direita do mouse:

<img src="https://i.ibb.co/bHLkcNj/Screenshot-1.png" alt="Screenshot-1" border="0">

**O script para rotacionar o Cubo, está presente abaixo**

```javascript

<img src="https://i.ibb.co/y60N0yw/gif2-gif.gif" alt="gif2-gif" border="0">
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
```
O script para movimentar o cubo, aplicando gravidade, é o abaixo:

```javascript


using System.Collections;

using System.Collections.Generic;

using UnityEngine;

public class Movimento : MonoBehaviour

{

    // Start is called before the first frame update

    Vector3 Vec;

    void Start()

    {

        

    }



    // Update is called once per frame

    void Update()

    {

        Vec = transform.localPosition;

        Vec.y += Input.GetAxis("Jump") * Time.deltaTime * 5;

        Vec.x += Input.GetAxis("Horizontal") * Time.deltaTime * 5;

        Vec.z += Input.GetAxis("Vertical") * Time.deltaTime * 5;

        transform.localPosition = Vec;

    }

}
```

**Para definir a velocidade da rotação, dentro do unity, adicione um script com o texto acima e nas opções: X, Y, Z, coloque a velocidade desejada**

<img src="https://i.ibb.co/Dg1PZmd/rota-o.png" alt="rota-o" border="0">
