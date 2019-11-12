# Rekognition
Avisa no Slack quando uma imagem é adicionada no bucket da S3.

Neessário ter um bucket na Amazon S3 com uma pasta com o nome de imagens, uma collection com o nome de Faces e um app no Slack

Crie uma lamnda function e faça o upload do rekognition.zip.
Adicione o nome do bucket, nome da collection, token do app do Slack e o um canal do Slack;
Crie um gatilho para a função esperando um evento em "images/" com o sufixo ".jpg"


Salve a função e adicione uma foto ao bucket para criar uma tabela no DynamoDB. Confira no mesmo se a tabela foi criada e adicione um # em return createTable() (linha 33)

Adicione mais uma foto para que seja criado uma Face no serviço Rekognition.

