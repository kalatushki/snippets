# snippets

Array.prototype.shuffle1 = function( deep )
{
  var i = this.length, j, t;
  while(i)
  {
   j = Math.floor( (i--) * Math.random() );
   t = deep && typeof this[i].shuffle!=='undefined' ? this[i].shuffle():this[i];
   this[i] = this[j];
   this[j] = t;
  }
  return this;
};