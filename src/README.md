# docker run --name database -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres

yarn sequelize migration:create --name=create-user
yarn sequelize db:migrate:undo
yarn sequelize db:migrate:undo:all
yarn sequelize db:migrate

yarn sequelize migration:create --name=create-files
yarn sequelize migration:create --name=add-avatar-field-to-users

yarn sequelize migration:create --name=create-appointments

#Aula 07

docker run --name mongobarber -p 27017:27017 -d -t mongo
