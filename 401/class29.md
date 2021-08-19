# Read: 29 - Room

## [Saving data with Room](https://developer.android.com/training/data-storage/room)
- Is like when to cache data so that when the device cannot access the network, the user can still browse that content while they are offline.

- With room we use SQL queries.


### Setup
- To use Room in your app, add the following dependencies to your app's build.gradle file:

```
dependencies {
    def room_version = "2.3.0"

    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"

    // optional - RxJava2 support for Room
    implementation "androidx.room:room-rxjava2:$room_version"

    // optional - RxJava3 support for Room
    implementation "androidx.room:room-rxjava3:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // optional - Test helpers
    testImplementation "androidx.room:room-testing:$room_version"

    // optional - Paging 3 Integration
    implementation "androidx.room:room-paging:2.4.0-alpha04"
}
```

### Primary components
- **The three major components in Room:**
1. The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
2. Data entities that represent tables in your app's database.
3. Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

### Sample implementation

1. **Data entity**
```
@Entity
public class User {
    @PrimaryKey
    public int uid;

    @ColumnInfo(name = "first_name")
    public String firstName;

    @ColumnInfo(name = "last_name")
    public String lastName;
}
```
2. **Data access object (DAO)**

```
@Dao
public interface UserDao {
    @Query("SELECT * FROM user")
    List<User> getAll();

    @Query("SELECT * FROM user WHERE uid IN (:userIds)")
    List<User> loadAllByIds(int[] userIds);

    @Query("SELECT * FROM user WHERE first_name LIKE :first AND " +
           "last_name LIKE :last LIMIT 1")
    User findByName(String first, String last);

    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);
}
```

3. **Database**
DataBase class must be like this:

```
@Database(entities = {User.class}, version = 1)
public abstract class AppDatabase extends RoomDatabase {
    public abstract UserDao userDao();
}
```

## [Defining entities in Room](https://developer.android.com/training/data-storage/room/defining-data)
## [Related entities in Room](https://developer.android.com/training/data-storage/room/relationships)
## [Accessing data with Room](https://developer.android.com/training/data-storage/room/accessing-data#java)