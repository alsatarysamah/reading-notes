# Associations

**Types:**

1-The HasOne association

2-The BelongsTo association

3-The HasMany association

4-The BelongsToMany association

**Defintion:**

const A = sequelize.define('A', /* ... */);

const B = sequelize.define('B', /* ... */);

A.hasOne(B); // A HasOne B

A.belongsTo(B); // A BelongsTo B

A.hasMany(B); // A HasMany B

A.belongsToMany(B, { through: 'C' });

**Terminology**

- The A.hasOne(B) association means that a One-To-One relationship exists between A and B, with the foreign key being defined in the target model (B).

- The A.belongsTo(B) association means that a One-To-One relationship exists between A and B, with the foreign key being defined in the source model (A).

- The A.hasMany(B) association means that a One-To-Many relationship exists between A and B, with the foreign key being defined in the target model (B).


- The A.belongsToMany(B, { through: 'C' }) association means that a Many-To-Many relationship exists between A and B, using table C as junction table, which will have the foreign keys (aId and bId, for example). Sequelize will automatically create this model C (unless it already exists) and define the appropriate foreign keys on it.

# Creating the standard relationships

- To create a One-To-One relationship, the hasOne and belongsTo associations are used together;

- To create a One-To-Many relationship, the hasMany and belongsTo associations are used together;

- To create a Many-To-Many relationship, two belongsToMany calls are used together

## One-To-One relationships

Foo.hasOne(Bar);

Bar.belongsTo(Foo);

**Options:**

Foo.hasOne(Bar, {

  onDelete: 'RESTRICT',

  onUpdate: 'RESTRICT'
});

Bar.belongsTo(Foo);

**Customizing the foreign key**

// Option 1

Foo.hasOne(Bar, {

  foreignKey: 'myFooId'

});

Bar.belongsTo(Foo);

// Option 2

Foo.hasOne(Bar, {

  foreignKey: {

name: 'myFooId'
  }
});

Bar.belongsTo(Foo);

# One-To-Many relationships

Team.hasMany(Player);

Player.belongsTo(Team);

**Options**

Team.hasMany(Player, {

  foreignKey: 'clubId'
});

Player.belongsTo(Team);
# Many-To-Many relationships

const Movie = sequelize.define('Movie', { name: DataTypes.STRING });

const Actor = sequelize.define('Actor', { name: DataTypes.STRING });

Movie.belongsToMany(Actor, { through: 'ActorMovies' });

Actor.belongsToMany(Movie, { through: 'ActorMovies' });

**Option**

Project.belongsToMany(User, { through: UserProjects, uniqueKey: 'my_custom_unique' })

# Association Aliases & Custom Foreign Keys

There are three ways to specify a different name for the foreign key:

1-By providing the foreign key name directly

2-By defining an Alias

3-By doing both things

# Special methods/mixins added to instances

Foo.hasOne(Bar)

fooInstance.getBar()

fooInstance.setBar()

fooInstance.createBar()




