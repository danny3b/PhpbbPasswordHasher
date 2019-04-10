Works for Phpbb 3.0.*


1. Save PhpbbPasswordHasher.php file in /src/Utility/

2. Place  in controller:

```
  use App\Utility\PhpbbPasswordHasher;
```

3. How to use it:

Checking password:

```
$hasher = new PhpbbPasswordHasher();
$check = $hasher->phpbb_check_hash($passwordToCheck, $existingPasswordInDatabase);
```

Hashing new password:

```
$hasher = new PhpbbPasswordHasher();
$newHash = $hasher->phpbb_hash($password);
```
