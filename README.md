Credit card fields for Django
=============================
django-creditcard-fields provides custom form fields for collecting and
validating credit card information.

Installation
------------

    pip install -e git+https://github.com/malteo/django-creditcard-fields.git#egg=django-creditcard-fields


Example usage
-------------

    from django import forms
    from django_creditcard.fields import CreditCardField, ExpiryDateField, VerificationValueField


    class PaymentForm(forms.Form):
        name_on_card = forms.CharField(max_length=50, required=True)
        card_number = CreditCardField(required=True)
        expiry_date = ExpiryDateField(required=True)
        card_code = VerificationValueField(required=True)


DISCLAIMER
----------
THIS SOFTWARE IS PROVIDED "AS IS". NO WARRANTY OF ANY KIND IS EXPRESSED OR
IMPLIED. YOU USE IT AT YOUR OWN RISK. IN NO EVENT SHALL THE AUTHORS BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE,
EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

ALSO, STORING CVV2 CODES IS **BAD**.
