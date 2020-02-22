<script>

</script>

<style>
  .info-tx {
    margin: 0 auto;
    max-width: 100%;
    padding: 5%;
    font-size: 30px;
    text-align: center;
    color: rgb(80, 80, 80);
    background-color: rgb(255, 255, 255);
  }
  .info-container {
    display: flex;
    flex-wrap: wrap;
  }
  .col-if {
    width: 50%;
  }
  .icon-container {
    display: flex;
  }
  p {
    margin: 0;
  }
  .info-display-tx {
    display: block;
    text-align: left;
  }
  .social-icons {
    display: flex;
  }
  .email-input, .tel-input {
  width: 100%;
  padding: 15px;
  margin: 5px 0 22px 0;
  display: inline-block;
  border: none;
  background: #f1f1f1;
  }
  .textarea-input {
  width: 100%;
  min-height: 50px;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}
.btn-submit{
  background-color: #4CAF50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>

<div class="info-tx">
  <h3>KONTAKTINFORMĀCIJA</h3>
  <div class="info-container">
    <div class="col-if">
      <div class="icon-container">

        <i class="material-icons">local_phone</i>
        <h4>
          <b>+371 29890312</b>
        </h4>
      </div>
      <div class="info-display-tx">Whatsapp - Viber - iMessage</div>
      <div class="icon-container">
        <i class="material-icons">contact_mail</i>
        <p>INFO@MODS.LV</p>
      </div>
      <div class="icon-container">
        <i class="material-icons">place</i>
        <p>RĪGA, BRĪVĪBAS GATVE 445F</p>
      </div>
      <div class="info-display-tx">
        Tikai ar iepriekšēju pierakstu. Klikšķiniet, lai palaistu navigāciju
        telefonā.
      </div>
    </div>
    <div class="col-if">
      <h2>SOCIĀLAJOS TĪKLOS</h2>
      <div class="social-icons">
        <i class="fa fa-facebook-official" aria-hidden="true" />
        <i class="fa fa-instagram" aria-hidden="true" />
        <i class="fa fa-youtube" aria-hidden="true" />
      </div>
    </div>
  </div>
  <div class="info-container">
    <div class="col-if">
<iframe width="425" height="350" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://www.openstreetmap.org/export/embed.html?bbox=27.7086353302002%2C56.54013232825401%2C27.741508483886722%2C56.553616977826266&amp;layer=mapnik&amp;marker=56.54687525346138%2C27.725071907043457" style="border: 1px solid black"></iframe><br/><small><a href="https://www.openstreetmap.org/?mlat=56.5469&amp;mlon=27.7251#map=15/56.5469/27.7251">Skatīt lielāku karti</a></small>    </div>
    <div class="col-if">
      <h2>ATPAKAĻSAITE</h2>
      <form action="/action_page.php">
    

    <label for="tel">Talrunis</label>
    <input class="tel-input" type="tel" id="tel" name="tel" placeholder="talrunis">

    <label for="email"><b>Email</b></label>
    <input class="email-input" type="text" placeholder="Enter Email" name="email" required>


    <label for="subject">Subject</label>
    <textarea class="textarea-input" id="subject" name="subject" placeholder="Write something.." style="height:100px"></textarea>

    <input class="btn-submit" type="submit" value="Submit">
  </form>
    </div>
  </div>
</div>
