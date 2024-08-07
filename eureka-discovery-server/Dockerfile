FROM maven as build

LABEL maintainer="OKORO MELLITUS"

WORKDIR /app

COPY . . 

RUN mvn install



FROM openjdk:11.0.10-jre

WORKDIR /app

COPY --from=build /app/target/eureka-0.0.1-SNAPSHOT.jar /app/

EXPOSE 9999

CMD [ "java","-jar","eureka-0.0.1-SNAPSHOT.jar" ]

