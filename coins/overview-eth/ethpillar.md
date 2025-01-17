---
descripción: >-
  Empoderado, inspirado, staker en casa. Gratis. Código abierto. Bienes públicos para Ethereum.
---

# 🛡️ EthPillar: herramienta de configuración de una sola línea y gestión de nodos TUI

{% hint style="success" %}
:heart: Apóyanos **en Gitcoin** GR20: [https://explorer.gitcoin.co/#/round/42161/26/34](https://explorer.gitcoin.co/#/round/42161/26/34)
{% endhint %}

## :new: ¿Qué es EthPillar?

:smile: **Instalador de nodo amigable**: ¿Aún no hay nodo? Le ayuda a instalar una pila de nodo Ethereum (Nimbus + Nethermind) en solo minutos. MEVboost incluido.

:floppy\_disk: **Facilidad de uso**: Ya no es necesario recordar los comandos de la CLI. Acceda a operaciones de nodo comunes a través de una interfaz de usuario de texto (TUI) simple.

:owl: **Actualizaciones rápidas**: Encuentre y descargue rápidamente la última versión de consenso/ejecución. ¡Menos tiempo de inactividad!

:tada:**Compatibilidad**: Detrás de escena, los comandos de los nodos y la estructura de archivos son idénticos a las configuraciones de staking V2.&#x20;

{% hint style="warning" %}
¿Ya tienes un validador? EthPillar es compatible con [una configuración de staking de Coincashew V2.](https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet)&#x20;
{% endhint %}

## :sunglasses: Vista previa

<figure><img src="../../.gitbook/assets/preview02.png" alt=""><figcaption><p>Menú Principal</p></figcaption></figure>

<div>

<figure><img src="../../.gitbook/assets/preview01.png" alt=""><figcaption><p>Cliente de ejecución</p></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/preview03.png" alt=""><figcaption><p>Cliente de consenso</p></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/preview04.png" alt=""><figcaption><p>Validador</p></figcaption></figure>

</div>

<div>

<figure><img src="../../.gitbook/assets/preview05.png" alt=""><figcaption><p>Administración del sistema</p></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/preview06.png" alt=""><figcaption><p>Herramientas</p></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/preview07.png" alt=""><figcaption><p>Mevboost</p></figcaption></figure>

</div>

## :whale: Prerrequisitos

* [Revisa cómo funciona el staking y los requisitos de hardware](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/prerequisites.md)
* Una instalación de [Ubuntu](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/prerequisites.md#setup-ubuntu).&#x20;
  * Probado trabajando con Ubuntu 22.04 LTS
  * También aparece compatible con Linux Mint 21.2, Debian 12

## :triangular\_ruler: Opción 1: Instalación automatizada de una sola línea

Abra una ventana de terminal desde cualquier lugar escribiendo .`Ctrl+Alt+T`.&#x20;

Para instalarlo, pegue lo siguiente:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/coincashew/EthPillar/main/install.sh)"
```

## :handshake: Opción 2: Instalación manual

**Instalar actualizaciones y paquetes:**

```bash
sudo apt-get update && sudo apt-get install git curl ccze bc tmux
```

**Clona el repositorio ethpillar e instala:**

```bash
mkdir -p ~/git/ethpillar
git clone https://github.com/coincashew/ethpillar.git ~/git/ethpillar
sudo ln -s ~/git/ethpillar/ethpillar.sh /usr/local/bin/ethpillar
```

#### Ejecute ethpillar:

```bash
ethpillar
```

## :tada:Próximos pasos

{% hint style="success" %}
¡Felicidades por instalar un EthPillar, lo que facilita el staking de nodos y casas!
{% endhint %}

<details>

<summary>Paso adicional para nuevos operadores de nodos, nuevos validadores</summary>

**Paso 1: Configura tu red, reenvío de puertos y firewall.**&#x20;

* Con EthPillar, la configuración se puede cambiar en:
  * **Herramientas > UFW Firewall > Habilitar firewall con la configuración predeterminada**
  * El reenvío de puertos [se configura manualmente](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-2-configuring-node.md#configure-port-forwarding), dependiendo de su enrutador.
  * Confirmar que el reenvío de puertos funciona con **Tools** > **Port Checker**
* Alternativamente, configure manualmente según la guía manual. [Haga clic aquí para ver la configuración detallada de la red.](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-2-configuring-node.md#network-configuration)

**Paso 2: Configura tu BIOS para que se encienda automáticamente después de una pérdida de energía**

Los pasos reales varían según el BIOS de su computadora. Idea general aquí:  [https://www.wintips.org/setup-computer-to-auto-power-on-after-power-outage/](https://www.wintips.org/setup-computer-to-auto-power-on-after-power-outage/)

**Paso 3: Habilitar la supervisión y las alertas (opcional)**

Se encuentra en:

* **Herramientas** > **Monitoreo**

**Paso 4: Comparar el nodo (opcional)**

Asegúrese de que el nodo tenga suficiente rendimiento de CPU/disco/red.

* **Herramientas** > **otro script de banco**

</details>

<details>

<summary>Pasos adicionales para los nuevos validadores</summary>

**Paso 1: Configurar las claves del validador**

* Familiarízate con la sección de la guía principal sobre la [configuración de tus claves de validación..](guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-5-installing-validator/setting-up-validator-keys.md)
* Cuando esté listo para generar sus claves, vaya a **EthPillar > Validator Client >  Generar / Importar claves de validador**

**Paso 2: Subir deposit_data.json a Launchpad**

* Para comenzar a apostar en Ethereum como validador, debe enviar al Launchpad su archivo de deposit_data.json, que incluye detalles cruciales de la dirección de retiro, y pagar el depósito requerido de 32ETH por validador.

**Paso 3: ¡Felicidades!**&#x20;

* Ahora estás esperando en la cola de entrada [https://www.validatorqueue.com](https://www.validatorqueue.com/)

<!---->

* Consulte los [siguientes pasos de la guía principal](https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/step-5-installing-validator/next-steps) para obtener más información. Especialmente las preguntas frecuentes "¿Recompensas de staking Wen?"
</details>

## :joy: POAP

Are you a EthPillar Enjooyer? [Support this public good by purchasing a limited edition POAP!](https://checkout.poap.xyz/169495)

<figure><img src="../../.gitbook/assets/3adf69e9-fb1b-4665-8645-60d71dd01a7b.png" alt=""><figcaption><p>Your EthPillar Enjoyoor's POAP</p></figcaption></figure>

**Purchase link:** [https://checkout.poap.xyz/169495](https://checkout.poap.xyz/169495)

ETH accepted on Mainnet, Arbitrum, Base, Optimism. :pray:

## :telephone: Get in touch

Have questions? Chat with other home stakers on [Discord](https://discord.gg/dEpAVWgFNB) or open PRs/issues on [Github](https://github.com/coincashew/ethpillar).&#x20;

Open source source code available here: [https://github.com/coincashew/EthPillar](https://github.com/coincashew/EthPillar)

## :heart: Donations

If you'd like to support this public goods project, find us on the next Gitcoin Grants.

Our donation address is [0xCF83d0c22dd54475cC0C52721B0ef07d9756E8C0](https://etherscan.io/address/0xCF83d0c22dd54475cC0C52721B0ef07d9756E8C0) or coincashew.eth

## :ballot\_box\_with\_check: How to Update

{% tabs %}
{% tab title="TUI Update" %}
Upon opening EthPillar,

* Navigate to **System Administration > Update EthPillar** and then quit and relaunch.
{% endtab %}

{% tab title="Manual Update" %}
From a terminal, pull the latest updates from git.

```bash
cd ~/git/ethpillar
git pull
```
{% endtab %}
{% endtabs %}

## :tada: Credits

Shout out to [accidental-green](https://github.com/accidental-green/validator-install) for their pioneering work in Python validator tools, which has unintentionally ignited the inspiration and direction for this project. We are building upon their innovative foundations by forking their validator-install code. A heartfelt thanks to accidental-green for their game-changing contributions to the open-source Ethereum ecosystem!
