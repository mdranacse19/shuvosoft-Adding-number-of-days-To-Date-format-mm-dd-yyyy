# shuvosoft-Adding-number-of-days-To-Date-format-mm-dd-yyyy
Html code :
                    <form class="form"  >
                            <div data-repeater-list="sickGoat" style="width: 103%;">
                                <div class="input-group mb-1 area_div" data-repeater-item>
                                    <div class="col-md-11">
                                        <div class="row">
                                            <div class="col-md-3">
                                                <div class="form-group " >
                                                    <label for="division " > Start Date :</label>
                                                    <div class="controls" >
                                                      <input type="date" id="start_Date" name="date" class="form-control" >
                                                    </div>
                                                </div>
                                            </div>

                                            <div class="col-md-3">
                                                <div class="form-group " >
                                                    <label for="division " >Set Days:</label>
                                                    <div class="controls" >
                                                        <input type="text" id="Set_days" onchange="getdate()" name="duration_day" class="form-control" >
                                                    </div>
                                                </div>
                                            </div>

                                            <div class="col-md-4">
                                                <div class="form-group " >
                                                    <label for="division " > Show Date :</label>
                                                    <div class="controls" >
                                                        <input type="text" id="set_days_from_date" name="set_days_from_date" class="form-control"   >
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </form>
                        
 --------------------------------                       
   #js code :
 -------------------------------
  <script>

        function getdate() {
            var set_date = document.getElementById('start_Date').value;
            var set_day_value = parseFloat(document.getElementById('Set_days').value);

            var newdate = new Date(set_date);

            newdate.setDate(newdate.getDate() + set_day_value);
            // alert(newdate.getDate())

            var dd = newdate.getDate('dd');
            if(dd < 10) {
                dd = '0'+dd;
            }
            var mm = newdate.getMonth('mm') + 1;
            if(mm < 10) {
                mm = '0'+mm;
            }
            var y = newdate.getFullYear();

            var someFormattedDate = mm  +'-'+ dd +'-'+ y ;
            // alert(someFormattedDate);
            document.getElementById('set_days_from_date').value = someFormattedDate;
        }
    </script>
