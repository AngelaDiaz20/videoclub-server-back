# videoclub-server-back

Inserte aquí documentación


```Connection Databases
const Connection = async (username, password) => {
    const URL = `mongodb://${Videoclub}:${movies}@movies.8wsfgdc.mongodb.net/?retryWrites=true&w=majority`;
    try {
        await mongoose.connect(URL, {useUnifiedTopology: true, useNewUrlParser: true});
        console.log('Database connected succesfully')
    } catch (e) {
        console.log('Error while connecting with the database', e)
    }
}

```
