---

copyright:

  years: 2015, 2018
lastupdated: "2018-02-05"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Ampliación de la CLI de {{site.data.keyword.Bluemix_notm}} con plug-ins
{: #plug-ins}

La CLI de {{site.data.keyword.Bluemix_notm}} da soporte a una infraestructura de plug-in para ampliar su capacidad. Puede instalar un plug-in desde un repositorio, un URL web, o instalar un binario del plug-in de forma local. 

[Repositorio de plugins de CLI de {{site.data.keyword.Bluemix_notm}}](http://clis.ng.bluemix.net/ui/repository.html#bluemix-plugins){: new_window} ![Icono de enlace externo](../../../icons/launch-glyph.svg) es el repositorio oficial donde se alojan los plugins.

Para obtener más mandatos para gestionar plug-ins, ejecute `bluemix plugin` para ver los mensajes de ayuda.
{: tip}

## Instalar un plugin desde el repositorio de la CLI de {{site.data.keyword.Bluemix_notm}}

### Paso 1: Busque el plugin

1. Utilice el mandato `bluemix plugin repo-plugins -r REPO_NAME` para buscar un plug-in en el repositorio.
2. La CLI de {{site.data.keyword.Bluemix_notm}} tiene el repositorio oficial con el nombre `Bluemix`, puede buscar los plugins oficiales como se muestra en el ejemplo siguiente:
  
  ```
  $ bluemix plugin repo-plugins -r Bluemix
  Getting plug-ins from repository 'Bluemix'...

  Repository: Bluemix
  Name           Description                                    Versions
  auto-scaling   IBM Cloud CLI plugin for Auto-Scaling service    0.2.1, 0.2.2
  nsg            IBM Cloud Network Security Group plugin          0.1.1

  ```

### Paso 2: Instale el plugin

Utilice el mandato `bx plugin install PLUGIN_NAME -r REPO_NAME` para instalar el plug-in. Por ejemplo, utilice el mandato siguiente para instalar un plugin desde el repositorio oficial de plugins de IBM `Bluemix`:

  ```
  $ bluemix plugin install auto-scaling -r Bluemix
  Looking up 'auto-scaling' from repository 'Bluemix'...
  9857792 bytes downloaded
  Installing plugin '/var/folder/v7/l3hnkz0x0b9b5mf1fyxh7yw00000gn/T/BluemixFileDownload062468676/auto-scaling-darwin-adm64-0.2.2'...
  OK
  Plugin 'auto-scaling 0.2.2' was successfully installed.
  ```

## Instale un plug-in de forma local

Utilice el mandato `bluemix plugin install LOCAL_FILE_NAME` para instalar el binario de un plugin en su máquina local. Por ejemplo:

  ```
  $ bluemix plugin install ./auto-scaling-darwin-amd64-0.2.2
  Installing pluign './auto-scaling-darwin-amd64-0.2.2'...
  OK
  Plugin 'auto-scaling 0.2.2' was successfully installed.
  $
  ```

## Instalar un plugin desde un URL de web

Utilice el mandato `bluemix plugin install URL` para instalar un plug-in directamente desde el URL de una web. Por ejemplo:

  ```
  ~$ bluemix plugin install https://plugins.ng.bluemix.net/downloads/bluemix-plugins/auto-scaling/auto-scaling-darwin-amd64-0.2.2
  Attempting to download the binary file...
  9857792 bytes downloaded
  Installing plugin '/var/folder/v7/l3hnkz0x0b9b5mf1fyxh7yw00000gn/T/BluemixFileDownload274645142/auto-scaling-darwin-adm64-0.2.2'...
  OK
  Plugin 'auto-scaling 0.2.2' was successfully installed.
  ~$
  ```
