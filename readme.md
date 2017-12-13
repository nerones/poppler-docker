# Poppler

Este repositorio contiene dos imagenes de docker que se pueden encontrar en
[docker hub](https://hub.docker.com/r/nerones/poppler-docker/):

* **nerones/poppler-docker:latest** La ultima version compilada de poppler
* **nerones/poppler-docker:pki-gob-ar** Una version modificada de poppler para
  que pueda validar documentos firmados con el [pki del gob argentino](https://pki.jgm.gov.ar/app/), se
  incluye tambien el certificado raiz y de la autoridad certificante disponibles en la [pagina oficial](https://pki.jgm.gov.ar/app/CertificateAuthority/RootCertificateDownload.aspx)
  Se puede ver la modificaion que se hizo en el [commit](https://github.com/nerones/poppler/commit/1bc1cffda53974210b9dbe846fa3f05a9618972b) de un fork propio.
  La idea de este tag es que se pueda validar directamente el pdf sin necesidad de instalar los certificados
  correspondientes en la maquina actual.


