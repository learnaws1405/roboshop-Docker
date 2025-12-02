FROM maven:3.9.11
EXPOSE 8080
WORKDIR /app/server
COPY pom.xnl .
COPY src ./src
RUN mvn clean package
COPY target/shipping-1.0.jar .
ENV CART_ENDPOINT="cart:8080" \
    DB_HOST="mysql"
CMD ["java", "-jar", "shipping.jar"]