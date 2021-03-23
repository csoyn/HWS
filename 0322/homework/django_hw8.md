# Django_hw8

> Django Accounts



### 1.  Django User Model

django에서 기본적으로 사용하는 User 모델은 아래의 경로에서 찾아볼 수 있다

```python
from django.contrib.auth.models import User
```

아래의 Django 공식 github 에서 User 모델이 정의된 코드를 찾아 작성하시오
https://github.com/django/django

```python
# Class User
class User(AbstractUser):
    """  Users within the Django authentication system are represented by this model.
    Username and password are required. Other fields are optional.  """
    class Meta(AbstractUser.Meta):
        swappable = 'AUTH_USER_MODEL'
        
# Class AbstractUser
class AbstractUser(AbstractBaseUser, PermissionsMixin):
    """ An abstract base class implementing a fully featured User model with admin-compliant permissions. Username and password are required. Other fields are optional.
    """
    username_validator = UnicodeUsernameValidator()

    username = models.CharField(
        _('username'),
        max_length=150,
        unique=True,
        help_text=_('Required. 150 characters or fewer. Letters, digits and @/./+/-/_ only.'),
        validators=[username_validator],
        error_messages={
            'unique': _("A user with that username already exists."),
        },
    )
    first_name = models.CharField(_('first name'), max_length=150, blank=True)
    last_name = models.CharField(_('last name'), max_length=150, blank=True)
    email = models.EmailField(_('email address'), blank=True)
    is_staff = models.BooleanField(
        _('staff status'),
        default=False,
        help_text=_('Designates whether the user can log into this admin site.'),
    )
    is_active = models.BooleanField(
        _('active'),
        default=True,
        help_text=_(
            'Designates whether this user should be treated as active. '
            'Unselect this instead of deleting accounts.'
        ),
    )
    date_joined = models.DateTimeField(_('date joined'), default=timezone.now)

    objects = UserManager()

    EMAIL_FIELD = 'email'
    USERNAME_FIELD = 'username'
    REQUIRED_FIELDS = ['email']

    class Meta:
        verbose_name = _('user')
        verbose_name_plural = _('users')
        abstract = True
```



### 2. Create user by ModelForm

새 유저를 생성하는 Django 내부에 정의된 ModelForm 을 사용하기 위한 import 구문을 작성하시오.

**답)** 

- 회원가입 `signup`에서는 `UserCreationForm`

+ `login` - `AuthenticationForm`
+ `update` - `UserChangeForm`

```python
from django.contrib.auth.forms import AuthenticationForm, UserCreationForm,UserChangeForm
```



### 3. Django sessions
Django 는 사용자가 로그인에 성공할 경우 (a) 테이블에 세션 데이터를 저장한다. 그리고 브라우저의 쿠키에 세션 값이 발급되는데 이 세션 값의 key 이름은 (b) 다.

**답)**  a - 데이터베이스 / b - session key