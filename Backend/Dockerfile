FROM eclipse-temurin:17-jdk

WORKDIR /app

COPY . .

RUN apt-get update && apt-get install -y maven

RUN chmod +x mvnw && ./mvnw clean package -DskipTests -Dmaven.test.skip=true

EXPOSE 8081

CMD ["java", "-jar", "target/*.jar"]
